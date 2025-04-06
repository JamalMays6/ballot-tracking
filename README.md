# Ballot Tracking

# 🗳️ Early Voting Ballot Tracker with Power Automate

This project automates the monitoring and reporting of ballot usage across multiple early voting sites using Microsoft Power Automate, Excel Online, and Outlook.

## 🧠 Problem
Election coordinators must monitor ballot usage daily across multiple locations and ensure accurate reporting. Manual tracking is error-prone and time-consuming.

## ✅ Solution
This solution uses Excel formulas and Power Automate flows to:
- Track daily ballot usage across 9 sites
- Automatically calculate remaining ballots
- Email daily summaries to stakeholders at 3 AM

## 📂 Files
- `BallotTracking.xlsx`: Main data file stored in OneDrive or SharePoint
- Power Automate Flows:
  - `Prepare Ballot Tracker Summary` – runs at 11 PM (optional)
  - `Send Daily Ballot Email` – runs at 3 AM daily

## 🛠 Tools Used
- Microsoft 365 Developer Account (Free)
- Power Automate
- Excel for Web
- Outlook 365

## 📊 Excel Sheet Structure

| Site | Starting amount | 4/22/2025 | ... | 4/29/2025 | UsedToday | Remaining |
|------|------------------|-----------|-----|-----------|------------|------------|

- `Remaining` is calculated via formula: `=B2-SUM(C2:J2)`
- `UsedToday` is calculated with `XLOOKUP` for today's date

## 📩 Email Output

Each morning at 3 AM, an email is sent with:

| Site | Used Yesterday | Remaining |
|------|----------------|-----------|
| EV1  | 270            | 1580      |
| ...  | ...            | ...       |

## 💼 Use Cases
- Election operations teams
- Inventory or supply chain daily monitoring
- Time-based resource tracking

## 🧪 How to Run
1. Sign up for a Microsoft 365 Developer account
2. Upload `BallotTracking.xlsx` to OneDrive
3. Format it as a table and name it `BallotLog`
4. Build the flows or import the templates

## 👤 Author
*Jamal Mays* – Election Coordinator | RPA Enthusiast | Microsoft 365 Developer
