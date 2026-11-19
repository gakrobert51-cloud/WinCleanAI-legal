# WinCleanAI Privacy Policy

**Effective date:** 18 November 2026
**Last updated:** 18 November 2026
**Controller:** Robert Gak
**Contact:** robertgak18@gmail.com

## 1. Scope and summary

WinCleanAI is a Windows 11 cleanup utility distributed through Microsoft Store. It
includes the desktop application, the cleanup engine, and the `winclean`
command-line tool (together, the "App"). This policy explains how Robert Gak
("WinCleanAI", "we", "us") handles information in connection with the App and
this website. It does not cover Microsoft's own handling of Store account,
installation, update, or crash data; Microsoft's privacy statement applies to
those services.

WinCleanAI is designed to work entirely on your device:

- The App works offline. Scanning, policy decisions, quarantine, restore, audit
  verification, and cleanup do not require a network connection.
- We do not collect, receive, store, sell, or share personal data through the
  App.
- The App contains no telemetry, analytics, advertising, crash-reporting SDKs,
  cloud AI, or remote file upload.
- No account or sign-in is required.
- Microsoft handles Store downloads, installations, updates, and any
  Store-related diagnostic data under its own privacy statement.

Because the App does not send us data, there is no server-side WinCleanAI
account, profile, or database about you.

## 2. Data processed locally on your device

The App processes the following data locally to perform its functions. It is not
transmitted to us or to any third party.

| Data | Purpose | Location |
|---|---|---|
| File metadata: name, path, size, timestamps, attributes, hashes | Scan, policy decision, and cleanup preview | Your device |
| Quarantine payload and metadata | Recoverability and verification | `%LOCALAPPDATA%\WinCleanAI\Quarantine` |
| Audit records: actor SID, operation, path, decision, hashes | Tamper-evident record of cleanup actions | `%LOCALAPPDATA%\WinCleanAI\Logs` |
| Audit HMAC key | Audit integrity verification | DPAPI `CurrentUser`; same directory |
| Settings and cleanup-zone configuration | App behavior | Your device |
| Engine log | Start-up and connection diagnostics | `%LOCALAPPDATA%\WinCleanAI\Logs\engine.log` |

The audit log is a local operational record. It can contain personal data such as
your Windows user SID and file paths. It stays on your device. In the Store
(MSIX) build, the App and engine run as the signed-in standard user, and local
data is access-controlled to `SYSTEM` and the current user.

Uninstalling the App intentionally leaves quarantine and audit data in place so
that a reinstall can recover it. You can remove the data at any time by deleting
`%LOCALAPPDATA%\WinCleanAI` or by using the App or CLI.

## 3. No telemetry, analytics, or cloud processing

The App does not:

- send usage statistics, crash reports, or diagnostic logs to us;
- use advertising or analytics SDKs;
- call a cloud AI service;
- upload file names, paths, hashes, or file content;
- perform update checks (Microsoft Store delivers updates).

Cleanup decisions are made by a deterministic policy engine on your device. A
future version may add optional local analysis features; this policy and the App
will be updated before any such feature is enabled.

## 4. Network access

The core features do not require network access. The App may use the network only
when you explicitly choose to:

- open a `mailto:` support link, in which case your email client handles the
  message;
- open a web link in this policy or the Store listing, in which case your
  browser handles it.

Microsoft Store itself may use the network to install or update the App and may
collect standard installation and crash information under Microsoft's privacy
statement.

## 5. Support emails

If you email robertgak18@gmail.com, we receive your email address, the content of
your message, and any attachments you choose to send. We use this information
only to respond to your request, troubleshoot the issue you report, and keep a
record of the support case.

- **Legal basis (EEA/UK):** our legitimate interest in providing support, or your
  consent where you choose to contact us; legal obligations where applicable.
- **Retention:** until the support case is closed, then up to 30 days, unless a
  longer period is required by law.
- **Sharing:** email is handled by our email provider, Google (Gmail), under
  Google's terms and privacy safeguards. We do not sell support emails or use
  them for advertising.
- **International transfers:** your email provider and ours may process messages
  outside your country, including in the United States, using the provider's
  safeguards.

Please do not send file contents, quarantine payloads, passwords, or other
sensitive information that is not necessary for your support request. The App's
Settings page can generate a short diagnostics text locally; you decide whether
to copy it into your email.

## 6. Microsoft Store

WinCleanAI is offered as a free listing. Microsoft processes Store account,
purchase, installation, update, and crash data under its own privacy statement.
We do not receive payment card details because the App is free. If a paid
offering is introduced later, this policy will be updated before it is offered.

## 7. Legal bases and your rights (EEA/UK)

Where the GDPR or UK GDPR applies:

- The App's local processing is controlled by you on your device. We do not
  receive that data.
- For support emails, we rely on the legal bases described in section 5.
- You may request access to, correction of, or deletion of your support emails,
  object to or restrict their processing, or withdraw consent.
- You may lodge a complaint with your local supervisory authority.

To exercise these rights, contact robertgak18@gmail.com. We may need to verify
your identity. You can delete local App data directly at any time from
`%LOCALAPPDATA%\WinCleanAI`.

## 8. Retention

| Data | Retention |
|---|---|
| Support emails | Until the case is closed, then up to 30 days |
| Local audit log | 30 days by default; daily seals are retained |
| Local quarantine | 30 days or a 10 GiB cap, whichever comes first |
| Local engine log | Until rotated or deleted by you |
| Store records | Handled by Microsoft; not applicable to the free listing |

## 9. Sharing

We do not sell personal data. We share data only:

- with Microsoft, for Store distribution, certification, installation, updates,
  and Store-related reporting under Microsoft's terms;
- with our email provider, Google, when you contact support;
- with authorities or professional advisers when required by law or necessary to
  establish, exercise, or defend legal claims.

We do not share local file metadata, quarantine payloads, or audit records with
advertisers, data brokers, or AI providers.

## 10. Security

We use Microsoft Store package signing and distribution, NTFS access controls for
local data, DPAPI for the audit key, and TLS for email and this website. The audit
log is tamper-evident through a hash chain and HMAC. In standard-user mode, the
same Windows user could technically rewrite local files, so the audit log is an
operational record rather than a defense against the device owner. No system is
perfectly secure. If you discover a vulnerability, contact
robertgak18@gmail.com.

## 11. Children

WinCleanAI is a professional utility and is not directed to children under 13 (or
the applicable age of digital consent). We do not knowingly collect children's
data.

## 12. Changes

We may update this policy to reflect product or legal changes. We will post the
new version on this page and update the effective date. Material changes will be
communicated in the App or on the Store listing.

## 13. Contact

Robert Gak
robertgak18@gmail.com

Publisher details are also shown on the Microsoft Store listing. This website uses
no cookies, analytics, or external resources.
