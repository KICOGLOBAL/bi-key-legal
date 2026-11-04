# BI-KEY Terms of Use

Version 0.14 · 4 November 2026 · Effective date: 5 November 2026

## 1. Publisher and purpose

The publisher and rights holder of BI-KEY is **„КИКО ГЛОБАЛ“ ЕООД / KICO GLOBAL EOOD**, Bulgaria ("Kico Global"). UIC (EIK): 208250164. VAT number: BG208250164. Registered office: Republic of Bulgaria, Varna, Odessos District, 1 Bacho Kiro Blvd., Floor 8, Office VIII-3. Contact: [kicoglobal@gmail.com](mailto:kicoglobal@gmail.com).

BI-KEY generates TOTP one-time codes and lets you respond to sign-in requests through compatible gateways. Kico Global supplies the app, does not provide or operate authentication gateways, and does not manage your external service accounts.

A local BI-KEY record does not by itself create an account with Kico Global or an external service.

## 2. Licence

Kico Global grants a non-exclusive right to install and use the app on your devices to authenticate accounts you are entitled to use, including work accounts.

Rights in the app and its branding remain with their respective rights holders. Open-source components are governed by their licences, available through Settings → Component licences. These terms do not restrict rights granted by those licences or mandatory law.

Relevant store terms also apply to downloading and using the app through that store. Apple's applicable standard licence agreement remains effective within its scope.

The app is not intended for children. If these terms are materially breached, Kico Global may terminate the licence by notice; after that the app may not be used.

## 3. Connecting accounts

Check the QR code's source and the gateway address before connecting. An organisation name in a QR code does not authenticate its sender. BI-KEY protocol compatibility does not mean that Kico Global has vetted the gateway operator.

Check records received from a backup file in the same way: the file may have been modified or created by someone else. Import files only from sources you trust and check the gateway address before connecting push.

Connecting push transfers the information described in the Privacy Policy. You can choose Codes only. Push requires a compatible gateway protocol and authority to send notifications for the relevant app. An arbitrary QR gateway address does not guarantee this capability.

## 4. Security and access

Use the app only for accounts you are authorised to access. Protect your device with a screen lock and keep secrets, setup QR codes and one-time codes confidential.

Approve only sign-in requests you initiated or reliably recognise. If you lose your device, tell the relevant service operator so it can revoke the binding.

Correct TOTP calculation depends on record settings and device time. Set up recovery methods provided by the external service in advance. The app's network functions do not send your local secrets to Kico Global, which cannot restore them from its database. Do not send secrets or current codes to support.

Uninstalling, resetting or replacing a device may cause loss of access to codes. BI-KEY does not provide cloud synchronisation. Kico Global does not keep a copy of your TOTP secrets. You can create an encrypted backup file to move or save records. Recovery of external service access is determined by that service's operator.

A backup file contains secrets that give access to your accounts. Choose a strong password and keep the file and the password separately and safely. Anyone holding the file and the password gains access to the codes. Recovery of a forgotten password is impossible. Create a copy in advance: it does not replace recovery methods at external services.

## 5. Push and external services

Delivery depends on the network, OS settings, permissions, gateway availability, Apple APNs and Google FCM. The app creates a Firebase registration on Android only. Android scanning uses Google ML Kit and starts only after your consent; iOS scanning uses Apple system frameworks.

Successful gateway registration does not guarantee delivery of every notification. Sending approval does not guarantee successful sign-in: the external service makes the final decision. The selected gateway operator determines its service rules and data processing.

## 6. Privacy and deletion

Processing is described in the [Privacy Policy](https://github.com/KICOGLOBAL/bi-key-legal/blob/main/PRIVACY-POLICY.en.md), also accessible in Settings. Accepting these terms does not replace separate consent where required by law.

Deleting a record removes its local data but does not delete an external account or automatically revoke the gateway registration. After the last push record is removed, the Android app requests deletion of its FCM token and Firebase installation ID. Ensure that another sign-in method remains before deletion. Contact the gateway operator about gateway data and contact us about processing for which Kico Global is responsible.

Deleting a record or the app does not delete backup files you saved or sent. You choose the storage provider or recipient; its rules govern further storage and handling of the copy.

## 7. Availability and liability

Kico Global takes reasonable steps to maintain the app's operation and security. Uninterrupted operation, complete freedom from errors and compatibility with every device or gateway are not guaranteed. This does not displace mandatory requirements applicable to the app under applicable law.

To the extent permitted by law, Kico Global is not liable for losses caused exclusively by failures of an independent authentication gateway, the user's actions or the user losing their device, where those losses are not attributable to a breach of Kico Global's obligations.

These terms do not exclude or limit liability for intentional misconduct, gross negligence or any other liability that cannot lawfully be excluded or limited. Mandatory consumer rights and data protection rights remain unaffected.

## 8. Changes and ending use

You may stop using the app. Arrange alternative access to external services before removing it. Before uninstalling the app or changing devices, create a backup if you want to keep your local records.

The current version of the app is provided free of charge. Kico Global may introduce paid features, a subscription or advertising in new versions, and may change or discontinue the app. We give advance notice of material changes; new terms apply from their effective date, and you may stop using the app.

New terms are published with their version and effective date. We communicate material changes appropriately. Where law requires separate acceptance or consent, it is requested separately; continued use does not replace legally required consent.

## 9. Governing law

The law of the Republic of Bulgaria applies. If you are a consumer, this choice does not deprive you of mandatory protections that would apply without that choice, including the law of your habitual residence where applicable.

Jurisdiction is determined by applicable rules, preserving mandatory consumer rights. These terms do not impose mandatory arbitration or exclusive Bulgarian jurisdiction for every dispute.

## 10. Contact and current version

Questions, complaints and error reports: [kicoglobal@gmail.com](mailto:kicoglobal@gmail.com).

The current version is available through Settings → Terms of use and its [public document page](https://github.com/KICOGLOBAL/bi-key-legal/blob/main/TERMS-OF-USE.en.md).
