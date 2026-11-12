# PySnake

<p align="center">
  <img src="https://ngocdolphincom.wordpress.com/wp-content/uploads/2026/11/pysnake-icon.png?w=300" alt="Official PySnake application icon: a blue and cyan snake curled around a padlock on a dark navy background." width="112" height="112">
</p>

**A personal encrypted data vault for Windows.**

<sub>Windows-first · Local-first · In active development · Not production-ready</sub>

PySnake is being built as a focused place to keep important personal information and private files together in one local vault. The goal is to make sensitive records easier to organize and retrieve while keeping the experience clear, compact and under the user's control.

> **Development notice**
>
> PySnake has not been released. The latest documented development build is `0.1.0+12` (project checkpoint: **8 November 2026**). This is an engineering prototype, not a production password manager. **Do not use it to store real passwords, TOTP seeds, recovery codes, identity documents or other sensitive data.** There is no public download at this time.

---

## What PySnake is being built to manage

- **Passwords and login records** — usernames, passwords, URLs and custom fields.
- **Two-factor authentication** — TOTP/2FA records and related account information.
- **Personal information** — reusable identity and contact details.
- **Secure notes** — private notes with tags, categories and pinned items.
- **Documents and attachments** — files, images and other private material associated with vault records.
- **Structured templates** — purpose-built record types, with optional custom fields.
- **Data portability** — selected exports and a bundle import/export workflow designed to preserve records and attachments.

These capabilities are part of an evolving development build. Their presence in the project does not mean every workflow has passed final release or independent security verification.

## Product direction

### Local-first and user-controlled

PySnake is designed around a local vault rather than a developer-hosted account service. The intended access model uses a master passphrase, a PIN gate and an optional keyfile. The user remains responsible for keeping the required credentials and keyfile safe; there is no developer-held recovery key or server-side vault access in the product design.

### One integrated application

The product is intended to bring related workflows into one Windows desktop app, rather than asking users to install separate tools for each kind of private information.

The current application includes work on:

- A single encrypted-container model for vault data.
- Record templates, custom fields, notes and encrypted attachments.
- In-app viewing and editing workflows for DOCX, XLSX and PPTX documents.
- An internal Chromium-based browser integrated with the vault.
- Audio and video previews using the Windows media stack, with codec coverage still limited.

Some of these areas are still being integrated and tested. In particular, the internal browser's broader user experience and several end-to-end workflows remain unfinished.

## Screenshots from the development build

The following images are selected captures from the current Windows development build. They illustrate the account-template chooser and the integrated browser; they do **not** imply that every associated workflow has passed final acceptance.

### Account and record templates

<p align="center">
  <img src="https://ngocdolphincom.wordpress.com/wp-content/uploads/2026/11/pysnake-add-account-templates-public.png" alt="PySnake development interface showing the Add Item template chooser with login, payment card, bank account, crypto wallet, exchange, identity document, software licence, API key and SSH templates. Personal information in the original capture has been obscured." width="100%">
</p>

### Integrated internal browser

<p align="center">
  <img src="https://ngocdolphincom.wordpress.com/wp-content/uploads/2026/11/pysnake-internal-browser.png" alt="PySnake development window with an integrated Chromium-based browser displaying a web page inside the application. The browser account avatar has been obscured for privacy." width="100%">
</p>

The screenshots are illustrative development captures. Internal-browser workflows remain under active development.

## Current development status

**Project state:** active development — not a public beta and not ready for production use.

The latest project checkpoint available for this overview is dated **8 November 2026**. It records progress on the vault foundation and the internal browser, while also documenting unfinished browser workflows, incomplete end-to-end acceptance, package defects and outstanding security/release checks.

Before a public test build can be considered, the project still needs to complete and verify the remaining browser user paths, run the required post-integration test suite, produce a clean and verified Windows package, and close the remaining security and release gates.

No release date is being announced.

## Platform

- **Current target:** Windows 10/11, 64-bit.
- **Technology:** Flutter and Dart, with native Windows components where required.
- **Other platforms:** macOS, Linux, Android and iOS are not currently offered.

## Important security and testing limits

PySnake handles data that could be highly sensitive. The project therefore treats security, data integrity and recovery as release blockers rather than marketing claims.

At the current development checkpoint:

- The application has **not** passed its production release gate.
- The current `dist` package is explicitly marked **not shippable** and must not be used as a public download.
- A fresh full test run after the latest browser integration work is still required.
- Some browser user paths and failure scenarios remain unverified.
- Independent security review and legal review remain outstanding.
- The current build must not be treated as a substitute for a mature, independently reviewed password manager.

Please use synthetic test data only during development.

## Roadmap

Work is being organized around the following high-level milestones:

1. Complete the remaining internal-browser workflows and security boundaries.
2. Re-run full integration and regression testing against the integrated application.
3. Complete clean Windows packaging, manifest verification and release preparation.
4. Finish the outstanding security, legal and independent verification work.
5. Announce a test or public release only after the applicable gates have passed.

The roadmap is directional; it is not a delivery-date commitment.

## Project links

- **Product page:** [PySnake on NgocDolphin](https://ngocdolphincom.wordpress.com/pysnake/)
- **Publisher:** [NgocDolphin](https://ngocdolphincom.wordpress.com/)
- **Feedback and issue reports:** [GitHub Issues](https://github.com/ngocdolphin3275/PySnake/issues)

## Repository scope

This public repository is currently a **project-information page**. It contains the public product overview and status information; it does not publish the private application source code, development logs, test fixtures, vault data, build outputs or downloadable binaries.

---

<sub>PySnake · An independent NgocDolphin project · Development build 0.1.0+12 (documented checkpoint: 2026-11-08)</sub>
