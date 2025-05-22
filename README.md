# 🦷 Dental Clinic Appointment Booking Automation

A complete no-code automation to handle dental clinic appointment bookings using:

- Google Forms
- Google Sheets
- Google Apps Script
- Zapier (Formatter, Gmail, Calendar)
- Gmail with HTML Logo Email

---

## 📋 Google Form Link

[Click here to open the form](https://docs.google.com/forms/d/e/1FAIpQLSc1OYZLHLX9ph3tW4rpa5jzNA3JMW-7CeD2qGBgGoJje1XZ2g/viewform?usp=sharing&ouid=111986711217638136263)

---

## 🧭 Flow Overview

1. Patient submits appointment via **Google Form**
2. Data goes into **Google Sheet**
3. A **Google Apps Script** combines date + time into ISO format
4. **Zapier** watches the sheet:
   - Combines and formats date/time
   - Sends email via **Gmail** (with logo and HTML)
   - Creates Google Calendar event
5. Confirmation email sent to patient with appointment details

---

## 🖼️ Screenshots

All screenshots of the Zapier setup, Gmail output, and flow are in the `/screenshots/` folder, including:

- `dental-appointment-booking-draft.png` – Overall Zap structure
- Other UI step images from the workflow

---

## 📦 How to Use

1. Copy the Google Form
2. Link it to a Google Sheet
3. Paste the Apps Script to auto-fill combined datetime
4. Create the Zap using provided steps
5. Customize the Gmail HTML email with your clinic logo

---

## 💌 Email HTML Template

```html
<p style="text-align: center;">
  <img src="https://i.ibb.co/PsqvKq4p/image-1.jpg" alt="SMile Dental Clinic Logo" width="150" style="margin-bottom: 10px;" />
</p>
<p>Hi <strong>{{Full Name}}</strong>,</p>
<p>Your appointment for <strong>{{Appointment Type}}</strong> is confirmed on <strong>{{Preferred Date}}</strong> at <strong>{{Preferred Time}}</strong>.</p>
<p>🕒 <strong>Time:</strong> {{Preferred Time}}<br>
📍 <strong>Location:</strong> 123 Shank Colony, Hyderabad</p>
<p>If you need to reschedule, reply to this email or call us at <strong>+91-8888888888</strong>.</p>
<p style="margin-top: 20px;">– <strong>SMile Dental Clinic</strong></p>
```

---

Made with 💙 by Sumanth
