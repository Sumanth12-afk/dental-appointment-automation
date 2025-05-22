# 🦷 Dental Clinic Appointment Booking Automation

A complete no-code automation to handle dental clinic appointment bookings using:

- Google Forms
- Google Sheets
- Google Apps Script
- Zapier (Formatter, Gmail, Calendar)
- Gmail with HTML Logo Email


📷 Screenshots
All screenshots of the Zapier setup and Gmail output are in the /screenshots/ folder.
---

## 📋 Google Form Link

[Click here to open the form](https://docs.google.com/forms/d/e/1FAIpQLSc1OYZLHLX9ph3tW4rpa5jzNA3JMW-7CeD2qGBgGoJje1XZ2g/viewform?usp=sharing&ouid=111986711217638136263)

---

## 🛠️ Tools Used

- Google Forms
- Google Sheets
- Zapier (Free tier)
- Google Calendar
- Gmail

---

## 🚀 Step-by-Step Setup

### STEP 1: Google Form
Create a form with fields:
- Full Name  
- Email Address  
- Phone Number  
- Appointment Type  
- Preferred Date  
- Preferred Time  
- Any Medical Notes  

### STEP 2: Google Sheets
- Link the form to Google Sheets.
- Sheet name: `Appointment`
- Worksheet: `Form Responses 1`

### STEP 3: Google Apps Script
Add a script to combine Preferred Date + Time into ISO format.

### STEP 4: Zapier Automation

#### 1. Trigger: Google Sheets
- Trigger: New Spreadsheet Row

#### 2. Formatter by Zapier
- Action: Add/Subtract Time
- Input: Combined DateTime
- Expression: `+1h`
- Output Format: `YYYY-MM-DDTHH:mm:ssZ`

#### 3. Google Calendar
- Action: Create Detailed Event
- Start & End Time: Use formatted DateTime
- Summary: `{{Appointment Type}} – {{Full Name}}`
- Description: Phone + Notes

#### 4. Gmail
- Send confirmation email using HTML body with clinic logo
dental-appointment-automation-project/


## 📧 Sample Email Body (HTML)

```html
<p style="text-align: center;">
  <img src="https://i.ibb.co/PsqvKq4p/image-1.jpg" alt="Clinic Logo" width="150" />
</p>
<p>Hi <strong>{{Full Name}}</strong>,</p>
<p>Your appointment for <strong>{{Appointment Type}}</strong> is confirmed on <strong>{{Preferred Date}}</strong> at <strong>{{Preferred Time}}</strong>.</p>
<p>📍 Location: 123 Shank Colony, Hyderabad</p>
<p>Reply to this email or call us at <strong>+91-8888888888</strong> if you need to reschedule.</p>
<p>– <strong>SMile Dental Clinic</strong></p>





