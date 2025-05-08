# PtvAlert Web Version

## Project Overview

PtvAlert Web is a real-time event reporting and visualization platform based on Google Maps and Firebase. Users can add reports with images and descriptions on the map, and all users can see these reports in real time. Each report is displayed as an emoji marker on the map. Clicking the marker shows details, comments, edit, or delete options. Reports automatically disappear from the map and database 3 hours after creation.

## Key Features
- Real-time display of all user reports on the map (with emoji markers)
- Support for image upload and text description
- Comment, edit, and delete your own reports
- Reports automatically expire and disappear after 3 hours
- Danmaku (bullet screen) for latest announcements and traffic info
- Responsive design for both mobile and desktop
- **One-click switch between English and Chinese UI** (🌐 button at the top right, all main UI and dialogs switch instantly)
- **One-click translation for comments and descriptions** (auto-detect content language, click 🌐 to translate between English and Chinese)

## Usage

1. **Clone or download this project**
2. **Open `index.html`** (recommended to use a local server such as VSCode Live Server, http-server, etc.)
3. **Firebase and Google Maps will initialize automatically on first load**
4. **Switch UI language anytime using the 🌐 button at the top right**; all buttons, dialogs, and prompts will update instantly
5. **Click the "+ Add Report" button**, select a location on the map, fill in the description, upload an image, and click "Submit"
6. **Emoji markers will appear on the map**; click a marker to view details, comment, edit, or delete (only your own reports)
7. **Reports disappear automatically after 3 hours**
8. **Click the 🌐 button next to any comment or description to instantly translate it** (auto-detects language and translates between English and Chinese)

## Dependencies
- [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript/overview)
- [Firebase Realtime Database](https://firebase.google.com/docs/database)
- No backend server required; all data is synced in real time to Firebase

## Local Development & Deployment

1. **Get a Google Maps API Key**
   - Apply for and replace `YOUR_API_KEY` in the `<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY...` in `index.html`
2. **Configure Firebase**
   - Use your own Firebase project and replace the `firebaseConfig` in `index.html`
3. **Preview locally**
   - Recommended: use VSCode "Live Server" extension or `npx http-server`
   - Opening `index.html` directly in the browser may limit some features (e.g., image upload, geolocation)

## Notes
- This project is a pure front-end static implementation; all user data is publicly stored in Firebase
- Do not upload sensitive or private information/images
- For production deployment, configure your own domain, API keys, and Firebase security rules

## Contribution & Feedback
Feel free to submit issues or pull requests for suggestions or bug reports.

---

MIT License 