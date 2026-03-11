GCT EEE Batch 27 OD Portal

A simple OD (On Duty) submission portal built using Google Apps Script, HTML, and Google Sheets.
This portal allows students to submit OD requests with selected dates and upload proof via Google Drive.

Features

- Mobile-friendly interface
- Calendar-based OD date selection
- Tap to select / deselect OD dates
- OD type selection
  - Full Day
  - Morning Only
  - Afternoon Only
- Previous / Next month calendar navigation
- Display of selected OD dates
- Google Drive upload button for OD proof
- Drive link submission
- Prevents duplicate submissions by roll number
- Data stored automatically in Google Sheets

Tech Stack

- Google Apps Script
- HTML / CSS
- JavaScript
- Google Sheets (Database)
- Google Drive (File upload storage)

System Architecture

Student Browser
⬇
Google Apps Script Web App
⬇
Google Spreadsheet Database

The form is hosted as a Web App using Google Apps Script and saves all submissions to a Google Sheet.

Setup Instructions

1. Create Google Spreadsheet

Create a sheet with the following columns:

Name | Roll Number | OD Details | Drive Link | Timestamp

2. Create Apps Script Project

Open the spreadsheet →
Extensions → Apps Script

Add the provided Code.gs and index.html files.

3. Deploy Web App

Deploy → New Deployment

Settings:

Execute As: Me
Who Has Access: Anyone

After deployment, copy the Web App URL and share it with students.

4. Google Drive Upload Folder

Create a folder in Google Drive where students upload their OD proof.

Paste the folder link inside the HTML upload button.

Usage Flow

1. Student opens the OD portal.
2. Enters Name and Roll Number.
3. Selects OD type (Full Day / Morning / Afternoon).
4. Chooses OD dates from the calendar.
5. Uploads proof to Google Drive.
6. Pastes the uploaded file link.
7. Submits the form.

The data is automatically stored in the Google Sheet.

Example Data Stored

Name| Roll| OD Details| Drive Link| Timestamp
Arun| 22EEE034| Mon Mar 10 (Full Day)| drive link| time

Capacity

The system easily supports 65+ students simultaneously since it uses Google Apps Script server infrastructure.

Future Improvements

- Disable past OD date selection
- Admin dashboard
- Automatic OD count
- Roll number verification
- File upload directly from portal

License

This project is open source for academic use.
