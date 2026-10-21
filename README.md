  # Privacy Policy — Accevate

  Accevate Technologies ("we," "our," or "us") operates the Accevate mobile application ("App"). This Privacy Policy explains how
  we collect, use, store, and protect your information when you use our App.

  ---

  ## 1. Information We Collect

  ### 1.1 Personal Information
  - Full name, email address, phone number, and employee code (provided by your organization during account setup)
  - Profile photo and selfies (captured for attendance verification)
  - Digital signatures (captured during visit verification)

  ### 1.2 Location Data
  - **Precise location (GPS):** Used for attendance check-in/check-out verification and visit tracking
  - **Approximate location:** Used for general area identification
  - **Background location:** Continuously tracks your route during active work visits and journeys to calculate distance traveled
  and verify site arrivals. Background tracking is initiated by the user (e.g., starting a visit) and runs via a foreground
  service with a visible notification
  - **Location accuracy, altitude, and speed** are recorded with each GPS data point
  - **Geofence verification:** Checks if the user is within the designated radius of a work site

  ### 1.3 Camera and Photos
  - Selfie photos for attendance verification
  - Site photos for visit documentation
  - Bill and receipt images for expense tracking
  - Work log images for daily reporting
  - Photos are compressed (max 1600px, 80% JPEG quality) before upload

  ### 1.4 Device Information
  - Device model and manufacturer
  - Operating system and version
  - Unique device identifier (UUID)
  - Screen resolution
  - App version number
  - Platform (Android/iOS)
  - Battery level (recorded with GPS data points)
  - Network connectivity status

  ### 1.5 Authentication Data
  - Login credentials (username and password)
  - OTP verification codes
  - Authentication tokens (access and refresh tokens)

  ### 1.6 Work and Activity Data
  - Attendance records (check-in/check-out times, locations, and distances)
  - Visit records including stages (journey start, arrival, check-in, work start/end, check-out, return)
  - Travel routes (complete GPS trajectory during visits)
  - Travel duration and distance calculations
  - Work logs with descriptions and photos
  - Expense records with categories, amounts, and receipt photos
  - Leave applications and balances
  - Daily work reports

  ### 1.7 Mock Location Detection
  - The App detects whether location data is being spoofed or mocked to ensure data integrity

  ---

  ## 2. How We Use Your Information

  We use the collected information for the following purposes:

  - **Attendance Management:** Verify employee check-ins and check-outs at authorized work locations using GPS location and selfie
   photos
  - **Visit Tracking:** Track and verify employee visits to assigned client sites, schools, or other locations, including travel
  routes and durations
  - **Route Recording:** Record GPS trajectories during work visits to calculate distance traveled and verify travel
  - **Work Documentation:** Enable employees to log work activities with descriptions and photos
  - **Expense Management:** Track and manage work-related expenses with receipt documentation
  - **Leave Management:** Process leave applications and track leave balances
  - **Reporting:** Generate daily work reports, attendance summaries, and operational analytics for the organization
  - **Push Notifications:** Send work-related reminders, approval updates, visit alerts, and system notifications
  - **App Functionality:** Authenticate users, maintain sessions, and provide core workforce management features
  - **Data Integrity:** Detect mock locations and verify GPS accuracy to ensure reliable attendance and visit data
  - **Navigation:** Provide driving directions and estimated arrival times to visit locations via Google Maps

  ---

  ## 3. Background Location Usage

  Accevate uses background location tracking for the following specific purpose:

  - When an employee **starts a visit or journey**, the App begins recording their travel route in the background
  - GPS data points are collected every **10 seconds** with a **50-meter distance filter**
  - Each data point includes latitude, longitude, speed, accuracy, altitude, battery level, and timestamp
  - Background tracking continues until the visit leg is completed (arrival at site or return to office)
  - A **persistent foreground notification** is displayed at all times during background tracking, showing navigation status and
  ETA
  - The tracking service may continue running after the app is closed and can **restart after device reboot** to ensure no data
  loss during active visits
  - Background location is **only active during user-initiated visits** — it does not track location continuously outside of work
  visits

  ---

  ## 4. Data Storage and Security

  ### 4.1 Local Storage
  - GPS data points are stored in a local SQLite database on the device before being synced to our servers
  - Authentication tokens are stored in encrypted secure storage (Expo SecureStore)
  - User profile data is cached locally for offline access
  - Pending sync items are queued locally and uploaded when connectivity is available

  ### 4.2 Data Sync
  - GPS route points are synced to our servers in batches of 50 points
  - Sync occurs at 2-minute intervals when the device has internet connectivity
  - Failed sync attempts use exponential backoff retry (up to 10 attempts)
  - Successfully synced data older than 7 days is automatically purged from local storage

  ### 4.3 Server Storage
  - All data is transmitted to our servers at `restapi.accevate.com` over encrypted HTTPS/TLS connections
  - Data is stored on secure servers with appropriate access controls
  - Data is retained only as long as necessary for the stated purposes or as required by applicable law

  ### 4.4 Security Measures
  - All network communication is encrypted using HTTPS/TLS
  - Authentication uses JWT tokens with automatic refresh
  - Each API request includes device identification and idempotency keys to prevent duplicate submissions
  - Biometric authentication (Face ID) may be used for additional security on supported devices

  ---

  ## 5. Data Sharing and Disclosure

  ### 5.1 We Do NOT
  - Sell your personal data or location data to third parties
  - Share your data with advertisers
  - Use your data for advertising or marketing purposes

  ### 5.2 We May Share Data With
  - **Your Organization's Administrators:** Authorized managers and administrators within your organization can view your
  attendance records, visit data, work logs, expenses, and location data as part of workforce management
  - **Service Providers:** We may share data with trusted service providers who assist us in operating the App (e.g., cloud
  hosting), under strict confidentiality agreements
  - **Google Maps:** Location data is sent to Google Maps APIs for driving directions, place search, and distance calculations.
  Google's privacy policy applies to this data
  - **Legal Requirements:** We may disclose data when required by law, court order, or to protect our legal rights

  ---

  ## 6. Third-Party Services

  The App uses the following third-party services:

  | Service | Purpose | Data Shared |
  |---------|---------|-------------|
  | Google Maps Directions API | Driving directions and ETA | Origin and destination coordinates |
  | Google Maps Places API | Location search and autocomplete | Search queries and current location |
  | Firebase Cloud Messaging | Push notifications | Device token |

  ---

  ## 7. User Rights and Controls

  ### 7.1 Device Permissions
  You can manage the following permissions through your device settings at any time:
  - **Location:** Grant or revoke precise location and background location access
  - **Camera:** Grant or revoke camera access
  - **Photos/Storage:** Grant or revoke access to photo library
  - **Notifications:** Enable or disable push notifications
  - **Microphone:** Grant or revoke microphone access

  **Note:** Disabling location permissions will affect attendance verification and visit tracking functionality. The App's core
  features require location access to operate.

  ### 7.2 Data Access
  - You can view your attendance history, visit records, and work logs within the App
  - For a complete copy of your data, contact your organization's administrator or reach out to us directly

  ### 7.3 Account and Data Deletion
  - To request deletion of your account and associated data, contact your organization's administrator or email us at the address
  below
  - Upon account deletion, your personal data will be removed from our active systems, subject to any legal retention requirements

  ---

  ## 8. Data Retention

  - **Active employee data:** Retained as long as the employee account is active with the organization
  - **Location and visit data:** Retained as necessary for business reporting and compliance purposes
  - **Local device data:** Synced data older than 7 days is automatically purged from the device
  - **Authentication tokens:** Cleared upon logout or session expiry

  ---

  ## 9. Children's Privacy

  Accevate is a workforce management application intended for use by adults (18 years and older) in a professional context. We do
  not knowingly collect personal information from children under the age of 18. If we become aware that we have collected data
  from a child, we will take steps to delete it promptly.

  ---

  ## 10. Auto-Start and Background Services (Android)

  On Android devices, the App may:
  - **Start automatically after device reboot** if an active visit/journey was in progress, to resume GPS tracking and prevent
  data loss
  - **Run a foreground service** with a visible notification during active location tracking
  - **Request exclusion from battery optimization** to ensure reliable background tracking during work visits

  These services only operate during active, user-initiated work visits and are not used for continuous surveillance.

  ---

  ## 11. Changes to This Privacy Policy

  We may update this Privacy Policy from time to time to reflect changes in our practices or for legal, operational, or regulatory
   reasons. We will notify users of significant changes through the App or by other appropriate means. The "Last Updated" date at
  the top of this policy indicates when the latest revisions were made.

  ---

  ## 12. Contact Us

  If you have any questions, concerns, or requests regarding this Privacy Policy or our data practices, please contact us at:

  **Accevate Technologies**
  - **Email:** info@accevate.com
  - **Website:** https://accevate.in
