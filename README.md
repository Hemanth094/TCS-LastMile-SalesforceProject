# 🏥 MediCare — Patient Appointment & Follow-Up CRM

A compact Salesforce Lightning application that helps healthcare teams manage doctor availability, schedule and track patient appointments, and handle follow-ups.

---

## 🚀 Key Features

- **Unified data model** for Doctors, Patients (Contacts), Appointments, and Medical Cases
- **Role-based access** (Admin, Doctor, Receptionist) with field-level security
- **Automation**: Record-triggered Flows for confirmations & reminders, Validation Rules, Quick Actions
- **Integrations**: Connected App + Named Credential; ready for SMS/EHR API callouts
- **Data quality & management**: Duplicate Rules, Import Wizard samples, deployment with SFDX/Change Sets
- **Observability & UI**: Reports, Dynamic Dashboards, and a reusable Lightning Web Component for appointment calendar

---

## � Quick Start

Prerequisites:
- Salesforce CLI (sfdx) installed and authenticated
- Node.js (LTS) and npm for LWC unit tests

Common tasks:

1. Install LWC dev dependencies

```bash
cd vscode/MediCareLWC
npm install
```

2. Run LWC unit tests

```bash
npm test            # runs sfdx-lwc-jest
```

3. Create and push to a Scratch Org (example)

```bash
sfdx force:org:create -f vscode/MediCareLWC/config/project-scratch-def.json -s -a MediCare
sfdx force:source:push
```

4. Execute sample Apex script or run a SOQL file

```bash
sfdx force:apex:execute -f scripts/apex/hello.apex
sfdx force:data:soql:query -q "$(cat scripts/soql/account.soql)"
```

---

## 🗂️ Project Layout (important paths)

- `force-app/main/default/classes/AppointmentController.cls` — Apex controller for appointment-related logic
- `force-app/main/default/lwc/appointmentCalendar/` — LWC component and unit tests (`__tests__`)
- `vscode/MediCareLWC/package.json` — test & lint scripts (use `npm test`, `npm run lint`)
- `vscode/MediCareLWC/config/project-scratch-def.json` — scratch org definition
- `scripts/apex/hello.apex`, `scripts/soql/account.soql` — helper scripts for manual testing

---

## ✅ Testing & Quality

- Run LWC unit tests: `npm test` from `vscode/MediCareLWC`
- Run Apex tests: `sfdx force:apex:test:run -r human`
- Lint/format changes: `npm run lint` and `npm run prettier`

---

## 🤝 Contributing

- Open an issue or send a PR with a clear description and tests where applicable
- Follow existing code style: run `npm run lint` and `npm run prettier` before committing
- Tests should pass locally (`npm test`) and Apex tests should be added for new server logic

---

