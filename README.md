# Meditro
This website tells you to take medicines.
# Meditro

## Apni bhasha mein, dawa ki yaad.

Meditro is a vernacular medicine and dose companion designed to help people take the right medicine, at the right time, in a language they understand.

Many people miss doses or take the wrong amount because medicine packaging is printed in small English text. This problem is especially difficult for senior citizens living alone and parents managing medicines for multiple family members.

Meditro converts a prescription routine into a simple visual and voice-based experience using medicine photos, dosage information, pill icons and spoken reminders.

## Problem Statement

People often face these problems:

- Medicine packaging is difficult to read because of small English text.
- Similar-looking tablets can be confused.
- People forget the correct time or quantity.
- Senior citizens may struggle to understand written instructions.
- Parents may need to manage medicines for multiple children.
- Caregivers do not always know whether a dose was taken.
- Existing medicine apps are often text-heavy and difficult to use.

## Our Solution

Meditro provides a visual, multilingual and accessible medicine routine.

Users can:

- Add a medicine using its photo.
- Store dosage, time, quantity and food instructions.
- View medicines using photos and visual cards.
- Receive spoken medicine reminders.
- Choose English, Hindi or Kannada.
- Manage routines for different family members.
- Use the Tablet Scanner to compare a tablet photo with saved medicine photos.
- Track taken, missed and pending doses.
- Use Elder Mode with a simpler interface and larger controls.

## Main Features

### 1. Visual Medicine Routine

Every medicine can include:

- Medicine name
- Medicine photo
- Tablet or capsule type
- Colour and shape representation
- Strength
- Quantity
- Reminder time
- Before-food, with-food or after-food instruction
- Starting stock
- Optional notes

This helps users understand their routine without depending only on English text.

### 2. Multilingual Voice Reminders

Meditro supports:

- English
- Hindi
- Kannada

The app can speak reminders such as:

> “It is time to take your medicine.”

The reminder can also include:

- Family member name
- Medicine name
- Dose quantity
- Food instruction

The app uses the device’s available speech voice. Users can also record or upload a custom voice reminder.

### 3. Medicine Alarm and Timer

The app includes a working alarm experience with:

- Medicine reminder popup
- Sound notification
- Spoken alert
- Hear Again option
- Snooze option
- Silence option
- Taken confirmation
- 10-second demo alarm for presentations

The demo alarm helps judges and users quickly understand how the product works.

### 4. Tablet Scanner

The Tablet Scanner allows users to:

- Open the camera
- Capture a tablet photo
- Upload an existing medicine image
- Compare it with medicine photos already saved in the routine
- See a possible visual match
- Add the scanned photo to a new medicine routine

The scanner uses local visual comparison with saved photos. It does not claim to identify an unknown tablet, diagnose a condition or replace a doctor, pharmacist or prescription label.

If no match is found, the user is asked to confirm the medicine from the packaging or prescription.

### 5. Family Profiles

Users can create separate medicine routines for:

- Parents
- Children
- Grandparents
- Other family members

Each profile has its own medicines, reminders and dose history.

### 6. Dose History

The history section shows:

- Taken doses
- Unconfirmed doses
- Snoozed doses
- Scheduled time
- Recorded time
- Family member
- Medicine quantity

A wrongly recorded dose can also be corrected.

### 7. Stock Tracking

Users can add the starting stock of a medicine.

Meditro can show:

- Remaining tablets
- Remaining capsules
- Remaining liquid quantity
- Low-stock warning

This helps families remember when a medicine may need to be purchased again.

### 8. Elder Mode

Elder Mode simplifies the interface by providing:

- Larger controls
- Easier navigation
- Clearer medicine cards
- Fewer distractions
- More visual information
- Better readability

### 9. Privacy-Focused Prototype

This prototype stores routines, photos and history in the browser’s local storage.

The Tablet Scanner compares images locally in the browser. No image is sent to an external medicine database in this prototype.

## How Meditro Works

1. The user selects a language.
2. The user selects a family member.
3. The user adds a medicine photo and prescription details.
4. The user selects dose quantity and reminder time.
5. Meditro displays the medicine as a visual routine card.
6. At the scheduled time, the app shows an alarm.
7. The app speaks the reminder in the selected language.
8. The user marks the dose as taken, snoozes it or listens again.
9. The dose is saved in the history section.
10. A caregiver can review the family routine and dose progress.

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript
- ES Modules
- Web Speech API
- MediaDevices API for camera access
- Canvas API for image processing
- FileReader API for image uploads
- LocalStorage for browser data persistence
- Node.js built-in test runner
- Python for portable website export

No external framework or third-party package is required for the basic prototype.

## Project Structure

```text
Meditro/
├── dist/
│   ├── index.html
│   ├── styles.css
│   ├── app.js
│   ├── domain.js
│   ├── translations.js
│   └── meditro-logo.png
│
├── scripts/
│   └── export-website.py
│
├── tests/
│   └── domain.test.mjs
│
├── package.json
├── README.md
└── .openai/
    └── hosting.json
```

## Getting Started

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
cd YOUR_REPOSITORY_FOLDER
```

### 2. Run the checks

```bash
npm run check
npm test
```

### 3. Start the local website

```bash
python3 -m http.server 8080 --directory dist
```

Open the following URL in your browser:

```text
http://localhost:8080
```

Camera and microphone features work best on:

- HTTPS websites
- Localhost
- A modern browser such as Chrome, Edge or Safari

## Creating the Portable Website

To create a single downloadable HTML file and ZIP package:

```bash
python3 scripts/export-website.py --output exports
```

This creates:

```text
exports/Meditro.html
exports/Meditro-Website.zip
```

The standalone HTML file contains:

- Website code
- CSS
- JavaScript
- Translations
- Logo
- Medicine interface

## Demo Instructions

1. Open the Meditro website.
2. Select English, Hindi or Kannada.
3. Open the Today page.
4. Click the 10-second alarm demo.
5. Listen to the spoken reminder.
6. Mark the medicine as Taken.
7. Open the Medicines section.
8. Add a medicine with a real package photo.
9. Open Tablet Scanner.
10. Capture or upload the same medicine photo.
11. Check the visual match result.
12. Open Family to view separate family routines.
13. Open History to view dose records.

## Hackathon Impact

Meditro focuses on accessibility, inclusion and medication safety.

The project helps:

- Senior citizens living alone
- Parents managing medicines for children
- Families supporting elderly members
- Users who are not comfortable reading English
- Caregivers who need a simple dose overview
- People who understand spoken instructions better than written instructions

The solution is intentionally simple, visual and language-friendly so that medicine routines do not depend only on reading small English labels.

## Safety and Limitations

Meditro is a prototype and not a medical diagnosis system.

Important limitations:

- It does not identify unknown medicines.
- It does not recommend medicines.
- It does not calculate a prescription dose.
- It does not replace a doctor or pharmacist.
- Users must confirm the medicine using the original packaging or prescription.
- Alarms require the browser tab to remain open.
- Browser and device settings may affect sound.
- Hindi or Kannada voice availability depends on the device.
- Camera access may require HTTPS or localhost.
- Browser local storage can be cleared by the user or browser.

## Future Improvements

Future versions can include:

- OCR for medicine labels
- Verified pharmacist confirmation
- Secure caregiver accounts
- Cloud backup with user permission
- WhatsApp or SMS caregiver alerts
- Offline-first mobile application
- More Indian languages
- Better pill-shape and colour recognition
- Prescription upload and structured extraction
- Smart medicine refill reminders
- Wearable and smart-speaker integration
- Accessibility support for vision-impaired users

## Project Status

Meditro is a working hackathon prototype demonstrating:

- Visual medicine routines
- Multilingual voice alerts
- Tablet photo scanning
- Family medicine profiles
- Dose history
- Stock tracking
- Elder-friendly interaction design

## Live Demo

[Open the Meditro Prototype](https://dozi-care-arfad.arfaad.chatgpt.site/)

## Team

**Project Name:** Meditro  
**Problem Statement:** Vernacular Medicine and Dose Companion  
**Team Members:** TEAM: 
2392608229 Vivek Raut
2392608217 Chiranth C R
2392608158 Manas Mahesh Rawool
2392608044 Prince Gupta
2392608162 Arfad 
**Hackathon:** Skyhawks

## Conclusion

Meditro makes medicine routines easier to understand through photos, icons, spoken alerts and local languages.

Its goal is simple:

> Help every person take the right medicine at the right time, in a language they understand.
