# HR Pro Enhanced — Standalone Prototype

A separate Expo / React Native prototype inspired by the uploaded HR Pro 1.3.3 package. It does not patch, replace, or access the original app.

## Features
- Home dashboard
- Anonymous Chat screen (local-only demo; no employee-to-employee delivery)
- Suggestion Box (entries saved only on this device)
- Employee Toolkit starter references
- AsyncStorage local persistence
- Separate Android application ID: `com.fercomz.hrproenhanced`

## Important limitations
There is no employee login, shared chat server, HR delivery, or company API integration. Local storage is not secure anonymity. Do not enter confidential company or employee information. Toolkit text is generic placeholder guidance, not official company policy.

A production version requires organization approval, authorized backend/API access, authentication, server-side authorization, moderation/reporting controls, a privacy notice, and security review.

## Build an installable APK (Expo EAS)
Requirements: Node.js 20.19.4+, npm, internet access, and an Expo account.

```bash
npm install
npx expo-doctor
npx eas login
npx eas build:configure
npx eas build --platform android --profile preview
```

The `preview` profile requests an installable APK. EAS supplies the APK download link after its cloud build completes.

## Run locally
```bash
npm install
npx expo start
```

## Identity
- Display name: HR Pro Enhanced
- Package ID: `com.fercomz.hrproenhanced`
- Version: `0.1.0`
- Original package ID found in supplied metadata: `com.silenttrader.HRProMobile`

## Build with GitHub Actions (Samsung / no PC)

This project includes `.github/workflows/android-apk.yml`.

1. Create a GitHub repository in your browser. Keep it **Private**.
2. Extract this ZIP on your phone.
3. In Termux, install Git and enter the extracted project folder.
4. Initialize Git, commit the project, add your GitHub repository as `origin`, and push the `main` branch.
5. In GitHub, open the repository, tap **Actions**, select **Build HR Pro Enhanced APK**, and tap **Run workflow**.
6. Wait for the workflow to finish with a green check.
7. Open that completed run, scroll to **Artifacts**, and download `HR-Pro-Enhanced-debug-APK`.
8. Extract the downloaded artifact ZIP; install `app-debug.apk` on your Samsung.

The workflow builds a debug-signed APK for testing. It does not create a Play Store release.
Do not upload keystores, passwords, employee data, API keys, or private company files to the repository.
