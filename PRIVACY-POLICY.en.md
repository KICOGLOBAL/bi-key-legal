# BI-KEY Privacy Policy

Version 0.14 · 4 November 2026 · Effective date: 5 November 2026

## 1. Who we are and what this policy covers

The publisher of the BI-KEY mobile app is **„КИКО ГЛОБАЛ“ ЕООД / KICO GLOBAL EOOD**, Bulgaria ("Kico Global", "we").

UIC (EIK): 208250164. VAT number: BG208250164. Registered office: Republic of Bulgaria, Varna, Odessos District, 1 Bacho Kiro Blvd., Floor 8, Office VIII-3. Contact for app and privacy matters: [kicoglobal@gmail.com](mailto:kicoglobal@gmail.com). No Data Protection Officer (DPO) has been appointed.

This policy covers the BI-KEY app and support correspondence. Kico Global does not provide or operate authentication gateways. You connect a gateway using connection details supplied by your organisation; its operator decides how it processes data and is responsible for that. Ask the organisation that issued the QR code for the operator's contact details.

We are responsible for processing whose purposes and means we determine ourselves: support correspondence and the Firebase project through which the app's push delivery works.

## 2. What is stored on your device

BI-KEY stores on the device: TOTP secrets, service and account names (which may contain a login or email address), code parameters, gateway addresses and binding identifiers, security settings, and service records of registration and previously handled requests.

- TOTP secrets, record names and logins, code parameters, gateway addresses and binding identifiers are kept in the operating system's secure storage. Record metadata created by earlier app versions (names, logins, parameters, gateway addresses) is moved there on first launch; if the move fails, it stays in ordinary app storage until the next attempt.
- App settings (including your QR-scanner choice and its time), service records of registration and the list of previously handled requests are kept in ordinary local app storage.
- The app creates a random installation identifier. It is not a phone number, IMEI or advertising identifier, and it differs from Firebase identifiers.

Codes are calculated on the device and need no internet connection. Original TOTP secrets, complete QR codes and the list of records are not sent to a Kico Global server. When you approve a push request, a calculated one-time code is sent to the gateway (see section 3). Integrated libraries may make their own network requests, for example when scanning QR codes on Android (section 4).

Backup. At your request BI-KEY creates a file containing your tokens (`.bikey`). It holds TOTP secrets, service and account names, code parameters and, for push records, the gateway address and binding identifiers. The backup contents are encrypted on the device with a password you choose. The app does not retain the password for later use or send it to Kico Global. Recovery of a forgotten password is impossible. Kico Global does not keep a copy of your TOTP secrets. Only a technical header (format version, encryption parameters, random values) is unencrypted.

## 3. Push: connecting and responding to requests

Before connecting, the app shows the gateway address from the QR code or backup, a data-transfer notice, and the buttons Connect, Codes only and Cancel. **A gateway may be located in any country, including outside the EEA, where data protection may differ from European standards.**

When you connect, the gateway receives: the user identifier from the QR code or backup, a random installation identifier, the notification token and the device type. The gateway also sees your IP address and technical connection information. After you choose to connect, the app may first check the gateway's API compatibility.

Notifications are delivered by Google Firebase Cloud Messaging (Android) and Apple Push Notification service (iOS). On iOS the app itself requests notification permission and obtains the APNs token; it does not create a Firebase registration and does not contact Firebase servers. The gateway operator writes the notification text, which may contain the service name, account label and other sign-in details. The message passes through the delivery provider.

A response sends the gateway the request identifier and your decision; approval also sends the calculated one-time code. The TOTP secret is not transmitted. HTTPS protects the connection to the gateway, but a push message is not end-to-end encrypted against the delivery provider.

Connect only to gateways of organisations you trust. Codes only does not register the record with the gateway. No Firebase Authentication account is created.

**Whether data is required.** Connecting push is optional. Without it, TOTP codes still work, and you can enter details manually instead of scanning. Push connection details can be obtained by scanning a QR code or importing a compatible backup. File import does not use the scanner. Importing does not itself connect push: each record requires separate confirmation showing the gateway address. Push needs the notification token and the installation identifier; without them push will not work.

Kico Global makes no automated decisions that have legal effects on you.

## 4. Apple, Google and GitHub

| Service | Use and information |
| --- | --- |
| Google Firebase / FCM (Android only) | Delivery registration, push tokens, installation identifiers, technical information. The FCM token is sent to the gateway. On iOS the app does not create a Firebase registration. |
| Apple APNs | iOS notification delivery: the device token and message content. iOS gateway registration uses the APNs token. |
| Google ML Kit (Android only) | QR recognition. Works only after your consent. Images and results are processed on the device; the SDK sends service metrics to Google. |
| Apple Vision / AVFoundation | Local camera operation and QR recognition on iOS. Frames are not uploaded to a recognition server. |
| Google Gmail | Support correspondence, if you write to our address. |
| System file selection, saving and sharing; the apps and cloud services you choose | The encrypted backup file is handled by the app or service you select under its own rules. Kico Global does not receive the file. |
| GitHub | Publication of documents. Opening a link connects your browser to GitHub, which handles technical visit information. The app appends no secrets to the link. |

ML Kit metrics may include device model, OS and app versions, an SDK installation identifier, events, errors, processing configuration and performance information. This is separate processing, unrelated to Firebase Analytics: disabling Analytics does not disable it.

The app does not use Firebase Analytics, Crashlytics, Firebase Authentication, Firestore, Cloud Storage or advertising SDKs. Integrated SDKs have their own retention rules.

Further information: [Firebase](https://firebase.google.com/support/privacy), [Firebase processing terms](https://firebase.google.com/terms/data-processing-terms), [ML Kit](https://developers.google.com/ml-kit/terms), [ML Kit metrics](https://developers.google.com/ml-kit/android-data-disclosure), [Apple](https://www.apple.com/legal/privacy/en-ww/), [Google, including Gmail](https://policies.google.com/privacy), [GitHub](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## 5. Camera, device-owner checks and clipboard

The camera reads QR codes only with your permission. On Android the scanner starts only if you have agreed to Google ML Kit (section 7). No video is recorded and no frames are uploaded to the gateway. You can enter TOTP details manually instead of scanning.

The operating system checks device ownership using biometrics or the device passcode. BI-KEY receives only the result, not biometric templates or your passcode. Device-owner verification is mandatory when exporting tokens and before accessing decrypted contents during import, regardless of the settings for app-opening and push-approval checks. If verification cannot be completed, the operation is unavailable.

At your request, a code is copied to the clipboard. The app uses available platform restrictions and an expiry period, but copies already read by another app cannot be revoked.

## 6. Where data is processed

Authenticator data on your device is processed on the device itself. The gateway operator determines the location and period of processing on the gateway; we do not claim where third-party gateways are hosted.

A backup file is kept where you saved or sent it: device storage, file storage, email or cloud. The storage provider or recipient you choose determines the country and retention period for that processing.

FCM runs on Google's global infrastructure; the app does not select a region. Apple, Google and GitHub may process technical information and messages in different countries, including the United States and countries in Europe. The publisher's Bulgarian registration does not mean that all data stays in Bulgaria or the EU.

Safeguards for transfers outside the EEA:

- Google states that Google LLC is certified under the EU-U.S. Data Privacy Framework; for Firebase, Google also publishes Standard Contractual Clauses (see [Firebase](https://firebase.google.com/support/privacy)).
- Apple and GitHub apply the mechanisms described in their policies (links in section 4).
- You can ask us for the terms that apply to processing for which we are responsible, using the contact address.

## 7. Purposes and legal bases (GDPR)

| Data | Purpose | Legal basis |
| --- | --- | --- |
| FCM token and Firebase installation identifiers (Android) | Delivering the push on Android that you requested by connecting a gateway | Performance of a contract (Terms of Use), Art. 6(1)(b) |
| Support emails and attachments | Answering enquiries, resolving problems, support security | Legitimate interests, Art. 6(1)(f): responding to users and fixing problems |
| ML Kit service metrics (Android only) | Operation of the QR scanner | Consent, Art. 6(1)(a): requested before the first scan, withdrawable in Settings |
| Data the law requires us to keep | Meeting a specific legal obligation | Art. 6(1)(c), only where such an obligation exists |

Backups are created and decrypted on your device at your request. The backup feature does not send the file or password to Kico Global. You choose where to save the encrypted copy or whom to share it with.

The APNs token (iOS) is not received or stored by Kico Global: Apple issues it, and the app passes it only to the gateway you choose.

Pressing Connect and the system notification permission are not blanket consent to all processing. If a specific operation needs consent, we will ask for it before processing starts; you may refuse and withdraw it at any time. Consent to the QR scanner on Android is requested before the first scan and can be withdrawn in Settings → Scan QR codes (Google ML Kit). Without consent the scanner does not open and you can add the token manually.

## 8. Retention and deletion

- **Local records** stay until you delete them. Deleting a record erases its metadata, secret and local binding information. The installation identifier and the list of previously handled requests are kept separately. Uninstalling the app does not guarantee removal of everything in the OS secure storage.
- **Backups.** Deleting a record or the app does not delete backup files you saved or sent. Retention by the selected recipient is governed by its rules. Recovery of a forgotten password is impossible.
- **Push.** After the last push binding is removed, the Android app requests deletion of the FCM token and the Firebase installation ID; on iOS there is no Firebase registration. The gateway registration is not deleted.
- **Firebase.** Retention is governed by Firebase's rules. After a deletion request, data is removed from live and backup systems within 180 days. If the request could not be sent (for example, no network) or the app was removed without deleting records, an Android FCM registration expires after 270 days of inactivity.
- **Gateway.** Deleting a record does not delete an external service account or revoke registration on the gateway. Contact the gateway operator for that.
- **Support.** Correspondence and attachments are deleted from the mailbox run by Kico Global (including Trash) no later than 30 days after the case is closed. Where law requires retention or a specific legal claim needs particular materials, we keep only what is necessary for a justified period. Deletion from Google's independent backup systems follows Google's terms.

Do not send us a TOTP secret for any purpose.

## 9. Your rights and contact

You may request information about processing, access, correction, deletion, restriction or portability, and object to processing based on legitimate interests. Where processing relies on consent, you may withdraw it; this does not affect the lawfulness of earlier processing. The scope of rights and exceptions depends on applicable law.

Contact: [kicoglobal@gmail.com](mailto:kicoglobal@gmail.com). To verify identity and find your registration we may ask for proportionate information. Do not send secrets, complete QR codes, current OTPs or your device passcode. Local secrets are not available to us and support cannot recover them.

You may complain to the **Bulgarian Commission for Personal Data Protection (CPDP / КЗЛД)**: [kzld@cpdp.bg](mailto:kzld@cpdp.bg), [contacts](https://cpdp.bg/en/contacts/). You may also contact another competent authority, including one where you habitually live or work, as provided by the GDPR.

## 10. Children, changes and current version

The app is not intended for children, and we do not knowingly process their data.

The current version is available in Settings → Privacy policy and on the [public page](https://github.com/KICOGLOBAL/bi-key-legal/blob/main/PRIVACY-POLICY.en.md).

We communicate material changes in processing appropriately; where separate consent is needed, we request it before such processing starts. The effective date is stated at the top of the document.
