# Automatic-data-cleaning-n8n
# Data Cleaning & Email Automation Workflow (n8n)

This workflow automatically collects messy data from Google Sheets, cleans and formats it using JavaScript, and sends a professional email using Gmail.

---

# Main Purpose

The main goal of this workflow is:

✅ Data Cleaning  
✅ Data Formatting  
✅ Message Sanitization  
✅ Email Automation  

---

# What This Workflow Cleans

The workflow automatically cleans:

- Extra spaces
- Uppercase/lowercase email issues
- Invalid symbols from messages
- Incorrect date formatting
- Unstructured text data

---

# Workflow Process

## 1. Google Sheets Trigger
Detects every newly added row automatically.

## 2. JavaScript Data Cleaning
The workflow cleans:

### Full Name
- Removes extra spaces
- Formats text properly

### Email
- Converts email to lowercase
- Removes unwanted spaces

### Amount
- Converts value into numeric format

### Date
- Converts date into clean YYYY-MM-DD format

### Message
- Removes extra spaces
- Removes weird/unwanted symbols
- Creates a cleaner version of the message

### Subject
- Uses custom subject
- Adds default subject if empty

---

# Example

## Raw Input Data

```json
{
  "Full Name": "   JOHN    DOE  ",
  "Email": " TEST@GMAIL.COM ",
  "Amount": "500",
  "Date": "5/8/2026",
  "Message": " Hello@@@    World!!! "
}
Clean Output Data
{
  "fullName": "JOHN DOE",
  "email": "test@gmail.com",
  "amount": 500,
  "date": "2026-05-08",
  "cleanMessage": "Hello World!!!"
}
Technologies Used
n8n
JavaScript
Google Sheets API
Gmail API
Security Features
No hardcoded passwords
OAuth credentials used securely
Safe data cleaning process
Removes unwanted characters from user input
Use Cases

This workflow can be used for:

Form data cleaning
Email automation
CRM preprocessing
Customer data formatting
Lead management systems
Automation learning projects
Author

Built for automation learning and data cleaning practice using n8n.
