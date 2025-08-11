## Payment Tracker

**Overview**
A simple payment tracker to monitor scheduled payments over time. It records dates, amounts, and status (Paid/Unpaid), auto-calculates totals, and shows a pie chart for quick status visibility.
-- 

# Features

* Tabular records: Date, Amount (₹), Status (Paid/Unpaid)

* Auto totals: Paid amount, Unpaid amount, and Grand Total

* Visual dashboard: Pie chart of Paid vs Unpaid

* Easy customization: Add rows, change dates/amounts, modify formulas

Example Snapshot

Paid Amount: ₹19,100

Unpaid Amount: ₹72,800

Total: ₹91,900

Status: Paid 20% | Unpaid 80%
(Add your screenshot below)
![Payment Tracker Dashboard](https://github.com/Suniljoshi-2003/Google-Sheet-Projects/blob/main/Payment%20tracker%20.png)

--

License
This project is open-source and free to use. You may modify and distribute with attribution..
--

##Contact
Author: Sunil Chandra Joshi
* Email : suniljoshi6360@gmail.com

* [LinkedIn](https://www.linkedin.com/in/suniljoshi2003) / [GitHub](https://github.com/Suniljoshi-2003)

--

Title: Tickets Tracker

Overview
Tickets Tracker is a simple spreadsheet-based solution (Excel/Google Sheets) to log, monitor, and visualize ticket status across their lifecycle. It helps track ticket IDs, owners, priority, status, due dates, and automatically summarize counts and SLA risks with a quick dashboard.

Features

Structured ticket log: Ticket ID, Title/Issue, Assignee, Priority, Status, Created On, Due Date, Comments/Notes

Auto summaries: Open vs Closed counts, Priority-wise distribution, Overdue tickets

Visuals: Pie/Bar charts for Status and Priority distribution (Excel/Sheets charts)

Filters and conditional formatting for quick scanning

Easy to customize and extend

File(s) in this repository

Tickets_Tracker Project.xlsx

README.md

images/ (optional: add screenshots of the dashboard or sample views)

Suggested Columns

Ticket ID

Title / Description

Assignee / Owner

Priority (High, Medium, Low)

Status (Open, In Progress, On Hold, Closed)

Created Date

Due Date

Resolution Date (optional)

SLA Breach? (Yes/No, formula driven)

Comments / Notes

How It Works (Formulas)
Use or adapt these formulas in Excel/Google Sheets:

Open Tickets count:
=COUNTIF(StatusRange,"Open")

Closed Tickets count:
=COUNTIF(StatusRange,"Closed")

Overdue (today > due date and not closed):
=COUNTIFS(StatusRange,"<>Closed",DueDateRange,"<"&TODAY())

Priority-wise counts (example for High):
=COUNTIF(PriorityRange,"High")

Completion Rate:
=COUNTIF(StatusRange,"Closed") / COUNTA(TicketIDRange)

If you track SLA in hours/days, add:

Days Open:
=IF([@Status]="Closed", [@ResolutionDate]-[@CreatedDate], TODAY()-[@CreatedDate])

Dashboard (Recommended)

Create summary cells for:

Total Tickets

Open / In Progress / On Hold / Closed

Overdue count

Priority split (High/Medium/Low)

Insert charts:

Pie chart for Status distribution

Bar chart for Priority-wise counts

Add slicers/filters (Excel) for Status, Priority, Assignee

Usage

Open Tickets_Tracker Project.xlsx

Go to “Data” sheet (or main table) and add/edit tickets in rows

View “Dashboard” sheet for aggregated counts and charts

Use filters to focus on assignee, priority, or status

Update status and dates as tickets progress; dashboard updates automatically

Best Practices

Use Data Validation:

Status: Open, In Progress, On Hold, Closed

Priority: High, Medium, Low

Conditional Formatting:

Highlight overdue tickets (DueDate < TODAY and Status <> Closed)

Color-code priorities

Freeze headers and protect formula cells

Keep a separate “Config” sheet for lists (Status, Priority) and thresholds (SLA days)

Customization Ideas

Add columns: Category/Module, Severity, Labels/Tags, Sprint, Client

SLA logic per priority (e.g., High = 2 days, Medium = 5 days)

Apps Script (Sheets) or VBA (Excel) to auto-stamp Resolution Date when Status becomes Closed

Export weekly summary as PDF for reporting

Getting Started (Google Sheets option)

Upload the Excel file to Google Drive and open with Google Sheets

Recreate data validation lists and conditional formats if needed

Update chart ranges and dashboard references

Screenshots
You can add screenshots to the repo and reference them like:
![Dashboard]()

License
This project is open-source. You may use, modify, and distribute it.

Contact
Author: Your Name
GitHub: your-profile
Email: your.email@example.com


