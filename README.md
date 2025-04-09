📄 Product Requirements Document (PRD)
🧠 Project Name
Project Financial Hub

🎯 Objective
Build an internal tool for the PMO team to manage and monitor project financials effectively by integrating with Notion databases, tracking resource hours, calculating real-time costs and profits, handling direct costs and payments, generating reports, and automating alerts.

👥 Users
PMO: Primary user managing finances, tracking hours, and adding direct costs.

PM: View access to financial status and KPIs.

Finance: Access to payments, exports, and overdue alerts.

Admin: Full access to configuration and integrations.

📌 Features
1. 🔄 Notion DB Sync
Sync user data (hourly rate, resource name) and worked hours per project.

Sync project info (name, tags, type: Monthly/One-time).

Manual trigger or automated sync (daily).

2. 🧑‍💻 Team Resources Management
Track hours and costs per project per user.

Derived from synced data.

Map hourly_rate * worked_hours to compute cost.

3. 🧱 Projects Configuration
Allow setting project type: Monthly or Fixed.

Assign client.

Add tags (e.g., "R&D", "Web", "Health").

Set estimated profits manually.

4. 👔 Clients Configuration
Create and manage client profiles.

Assign to projects and link to payments.

5. 💵 Payments Module
Fields: Name, Client, Amount, Status (Paid / Partial / Overdue / Due), Due Date, Note.

Auto-compute payment status.

Email reminders for overdue payments (configurable frequency).

Manual or bulk entry of payments.

6. 🧾 Direct Costs
Add non-hour-based project expenses (e.g., software licenses, hardware).

Manual entry by project.

Tracked and timestamped.

7. 📊 KPI Engine
Global and per-project KPIs:

Total Worked Hours

Total Cost (Resources + Direct)

Total Payments

ROI = Total Payments - Total Costs

Burn Rate = Total Cost / Duration

Estimated vs. Actual Profit

Forecasted Break-Even Date

8. 📅 Monthly Calculations (for Monthly Projects)
Automatically calculate:

Monthly cost breakdown

Monthly income from payments

Monthly ROI and Burn Rate

Monthly report view for each project

9. 📤 Export & Reporting
Export project financials to Excel or PDF

Models: Per project / All projects / Monthly report / Client-specific

Include charts and KPIs

10. 🚨 Alerts System
Overdue payments

Budget exceeded

Estimated profit not reached

Resource idle (no hours > 7 days)

Custom alerts based on project tags

🧱 Technical Requirements
Architecture
Backend: Node.js or Django (based on intern’s experience)

Frontend: React (with Tailwind), or admin dashboard framework

Database: PostgreSQL

Notion Integration: Notion SDK or REST API

Emailing: SMTP integration (SendGrid, Mailgun, etc.)

Scheduler: Cron jobs for daily syncs and overdue checks

🖼️ Wireframes / UX (To Be Designed)
Pages:

Dashboard (Global KPIs, Alerts)

Project Detail (KPI cards, monthly breakdown, direct costs, payments)

Payments Manager

Direct Costs Manager

Clients Manager

Exports & Reports

Settings (Notion, Email Alerts, etc.)

🧪 KPIs for This Tool
% of payments tracked and paid on time

Accuracy of projected vs actual profit

Time saved per month vs manual Excel workflow

PMO satisfaction score

