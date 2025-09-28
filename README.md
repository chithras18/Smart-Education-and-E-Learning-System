# Salesforce Student–Course–Assignment Management System

## 📌 Overview

This project is a Salesforce-based education management system designed to manage **Students, Courses, and Assignments**.
It covers the full lifecycle of a Salesforce project—from data modeling and configuration to UI enhancements and automation.

The project has been built in a **Developer Edition (DE) Org** and follows a structured phase-wise approach.

---

## 🚀 Features

* **Custom Objects**

  * Student (`Student__c`)
  * Course (`Course__c`)
  * Assignment (`Assignment__c`)

* **Key Relationships**

  * Student ↔ Course (via Enrollment/lookup)
  * Course ↔ Assignment
  * Assignment ↔ Student

* **UI Enhancements**

  * Custom Lightning Pages (Student Portal, Teacher Portal)
  * Quick Actions (e.g., *Add Assignment* from Course)
  * Custom Button (*Mark Complete* on Assignments)

* **Automation**

  * Validation rules (due dates, progress %)
  * Workflow rule with Email Alert (notify Teacher on new Assignment)

* **Reports & Dashboards**

  * Student Progress
  * Pending vs Completed Assignments
  * Course Enrollment Statistics

* **Security Review**

  * Teachers: Manage Courses & Assignments
  * Students: Limited read-only access to restricted fields

---

## 🏗️ Project Phases

### Phase 1–7: Core Setup

* Designed **custom objects & fields**.
* Established **relationships** between Student, Course, Assignment.
* Built **basic UI pages** and layouts.

### Phase 8: Data Management & Deployment

* Data Import Wizard for Students, Courses, Assignments.
* Data Export for backups.
* Set up VS Code + Salesforce CLI (SFDX) for version control.
* Ran Apex test classes (≥ 75% coverage).

### Phase 9: Advanced Functionality & UI Enhancements

* Added Quick Actions & Custom Buttons.
* Customized Lightning Pages with related lists and charts.
* Configured Validation Rules & Email Alerts.
* Built Reports & Dashboards.
* Performed Security Review on Profiles & Permission Sets.

---

## ⚙️ Setup Instructions


1. **Authorize Salesforce Org**

   ```bash
   sfdx auth:web:login -a MyDevOrg
   ```

2. **Deploy Metadata**

   ```bash
   sfdx force:source:push -u MyDevOrg
   ```

3. **Load Sample Data**

   * Use Data Import Wizard (Setup → Data Import Wizard).
   * Import `Course.csv`, then `Student.csv`, then `Assignment.csv`.

---

## 📊 Reports & Dashboards

* **Student Progress Report**: Tracks completion percentage across courses.
* **Assignment Status Report**: Pending vs Completed.
* **Course Enrollment Dashboard**: Visual overview of course engagement.

---

## 🔒 Security Model

* **Student Profile**: Read-only access to assignments and grades.
* **Teacher Profile**: Full control of Courses, Assignments, and Student Progress.
* **Admin Profile**: All objects + configuration rights.

---

## ✅ Testing

* Run all Apex tests:

  ```
  Setup → Apex Test Execution → Run All
  ```
* Verified workflows, validation rules, and dashboards.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo.
2. Create a feature branch.
3. Commit changes.
4. Submit a pull request.

---

## 📧 Contact

**Author**: Chithra Acharya 🪻
For queries, reach out via GitHub Issues or Discussions.
