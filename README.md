# Conditional Support Ticket Router

An intelligent triage automation that evaluates incoming support requests by priority level. It routes "Urgent" tickets to immediate email alerts while logging "Normal" requests to a centralized tracking sheet.

##  Architecture & Workflow
<img width="723" height="433" alt="image" src="https://github.com/user-attachments/assets/43d27aad-0441-4830-9976-c42dbd8a64e6" />

**Modules Used:**
* Google Forms (Trigger)
* Make.com Router (Conditional Logic)
* Gmail (Urgent Alerting)
* Google Sheets (Standard Logging)

##  How It Works
1. **Trigger:** A support ticket is submitted via Google Form with a "Priority" dropdown (Urgent/Normal).
2. **Routing Logic:** A Make.com Router evaluates the `Priority` field using conditional filters.
3. **Path A (Urgent):** If the ticket is marked "Urgent", an immediate, formatted alert email is sent to the support team.
4. **Path B (Normal):** If the ticket is "Normal", it is silently logged into a Google Sheets database for batch processing.

##  Business Value
* Automates IT/Support ticket triage without human intervention.
* Ensures critical issues receive immediate attention, reducing SLA breach risks.
* Keeps standard inquiries organized without cluttering email inboxes.

##  How to Import
1. Log in to your [Make.com](https://www.make.com/) account.
2. Create a new Scenario.
3. Click the menu (three dots) in the top right -> **Import blueprint**.
4. Upload the `blueprint.json` file from this repository.
5. Re-authenticate your Google account connections and update the email address in the Gmail module.
