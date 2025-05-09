# PtvAlert Web Version

## Project Overview

PtvAlert Web is a real-time event reporting and visualization platform based on Google Maps and Firebase. Users can add reports with images and descriptions on the map, and all users can see these reports in real time. Each report is displayed as an emoji marker on the map. Clicking the marker shows details, comments, edit, or delete options. Reports automatically disappear from the map and database 3 hours after creation.

## Latest Updates
- **Login Flow Optimization**:
  - Improved user login flow to ensure users must log in before accessing the map interface
  - Enhanced multilingual support for guest mode labels, ensuring they update automatically with language switching
  - Strengthened logout functionality to completely clear all login states
  - Optimized user menu display and interaction experience
- **Danmaku System Enhancement**:
  - Reduced danmaku movement speed for better readability (10-15 seconds to complete one movement)
  - Decreased danmaku display frequency to reduce information overload (2.5-second intervals)
  - Optimized danmaku visual styling: larger font, more prominent background, clearer text shadow
  - Increased spacing between danmaku messages to reduce overlapping and improve readability
  - Added border and shadow effects to ensure danmaku are visible against various backgrounds
- **Firebase Authentication System Optimization**:
  - Fixed Firebase authentication configuration issues
  - Removed automatic forced redirection to guest mode
  - Restored normal email/password registration and login functionality
  - Maintained guest mode as a quick access option
  - Enhanced login state verification logic to support multiple login methods
  - Improved error handling with more user-friendly error messages
  - Automatically offers guest mode as a fallback when Firebase is unavailable
  - Supports freely switching between regular login and guest mode

## Key Features
- **User Account System**
  - Email registration and login
  - Guest mode for access without registration
  - Profile management and password reset
  - Persistent login state
  - Simple and intuitive login/logout process
- Real-time display of all user reports on the map (with emoji markers)
- Support for image upload and text description
- Comment, edit, and delete your own reports
- Reports automatically expire and disappear after 3 hours
- **Enhanced Danmaku System**: Real-time display of transit announcements, service changes, and user reports
  - Multi-track danmaku design ensuring clear message visibility
  - Adjusted danmaku speed and display frequency for better reading experience
  - Optimized danmaku visual style for enhanced readability
  - Integration with YarraTrams service updates, including publication timestamps
  - Automatic inclusion of user reports and comments in the danmaku stream
  - Multiple styles to distinguish different message types (service changes, safety alerts, user reports, etc.)
  - Language switching that follows the system language setting
  - Automatic daily updates at midnight, with manual refresh option for latest information
- Responsive design for both mobile and desktop
- **One-click switch between English and Chinese UI** (🌐 button at the top right, all main UI and dialogs switch instantly)

## Usage

1. **Clone or download this project**
2. **Open `login.html`** (recommended to use a local server such as VSCode Live Server, http-server, etc.)
3. **Login System**:
   - Register a new account with email
   - Login with existing account
   - Select "Continue as Guest" to use without registration
4. **Firebase and Google Maps will initialize automatically on first load**
5. **Switch UI language anytime using the 🌐 button at the top right**; all buttons, dialogs, and prompts will update instantly
6. **Top danmaku area** displays latest tram service information and user reports; click the "Refresh Tram Info" button in the upper right to get the latest updates
7. **Click the "+ Add Report" button**, select a location on the map, fill in the description, upload an image, and click "Submit"
8. **Emoji markers will appear on the map**; click a marker to view details, comment, edit, or delete (only your own reports)
9. **Reports disappear automatically after 3 hours**
10. **User menu in the top right** allows you to manage your profile or log out

## Dependencies
- [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript/overview)
- [Firebase Realtime Database](https://firebase.google.com/docs/database)
- [Firebase Authentication](https://firebase.google.com/docs/auth)
- No backend server required; all data is synced in real time to Firebase

## Local Development & Deployment

1. **Get a Google Maps API Key**
   - Apply for and replace `YOUR_API_KEY` in the `<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY...` in `index.html`
2. **Configure Firebase**
   - Use your own Firebase project and replace the `firebaseConfig` in both `index.html` and `login.html`
   - Enable Email/Password and Anonymous authentication methods in your Firebase console
   - Detailed steps:
     1. Visit the [Firebase Console](https://console.firebase.google.com/)
     2. Create a new project or select an existing one
     3. Enable "Email/Password" sign-in method under "Build > Authentication > Sign-in method"
     4. Get your Firebase configuration object from "Settings > Project settings > Your apps > SDK setup and configuration"
     5. Copy the configuration to the `firebaseConfig` variable in both `login.html` and `index.html`
     6. Add your domain to "Authentication > Settings > Authorized domains" (add localhost for local development)
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