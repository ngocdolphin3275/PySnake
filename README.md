# PySnake

<p align="center">
  <img src="https://ngocdolphincom.wordpress.com/wp-content/uploads/2026/11/pysnake-icon.png?w=300" alt="Official PySnake application icon: a blue and cyan snake curled around a padlock on a dark navy background." width="112" height="112">
</p>

**A personal encrypted data vault for Windows.**

<sub>Windows-first · Local-first · In active development · Not production-ready</sub>

PySnake is being built as a focused place to keep important personal information and private files together in one local vault. The goal is to make sensitive records easier to organize and retrieve while keeping the experience clear, compact and under the user's control.

> **Development notice**
>
> PySnake has not been released. The latest documented development build remains `0.1.0+12` (build checkpoint: **8 November 2026**); no newer build identifier has been verified for this public update. This is an engineering prototype, not a production password manager. **Do not use it to store real passwords, TOTP seeds, recovery codes, identity documents or other sensitive data.** There is no public download at this time.

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
- In-app document viewing and editing workflows for DOCX, XLSX and PPTX.
- An internal Chromium-based browser integrated with the vault.
- Supporting audio and video previews using the Windows media stack, with codec coverage still limited.

The browser and document/media capabilities are supporting parts of the integrated application, not substitutes for completing and validating the core vault workflows. Some areas are still being integrated and tested.

## Screenshots from the development build

The following images are selected captures from the Windows development build. They illustrate the account-template chooser and the integrated browser; they do **not** imply that every associated workflow has passed final acceptance.

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

**Public status update:** 21 November 2026. The latest documented build checkpoint remains `0.1.0+12` from 8 November 2026; this update does not claim that a newer build has been produced or released.

The core vault and record-management workflows remain the main product focus. The integrated Chromium browser is present in the development build, but its interaction paths and regression coverage are not yet complete.

### Open browser issue under investigation

After a web page finishes loading, moving the pointer over the browser toolbar can cause the page content to disappear or become invisible. The root cause has not yet been established, and no fix has been verified. This issue remains open.

The investigation needs to cover more than an isolated hover event. Relevant interactions include:

- Toolbar hover and focus states.
- The browser content surface and its visibility, stacking and rendering behavior.
- Page loading and rendering lifecycle.
- Navigation, reload and recovery after a content display failure.
- Window resizing and adjacent UI state transitions.

Once the issue is reproduced and its root cause is fixed, regression coverage should be added for this defect and related browser paths. A narrow patch without validating neighboring states is not sufficient.

### Historical automated-test snapshot

The last recorded automated-test snapshot available in the project notes is dated **5 November 2026**, for build **0.1.0+9**:

| Check | Recorded result |
|---|---:|
| Automated tests passed | 363 |
| Automated tests skipped | 7 |
| Project validator | 1,157 checks |
| Static analyzer | Clean |
| Windows release build | Successful |

These are historical results for that checkpoint only. They do **not** establish that later browser integration changes pass the same tests, that the current development build is stable, or that PySnake is ready for release. A fresh full test run after the latest integration and fixes is still required.

### Release readiness and security limits

- The application has **not** passed its production release gate.
- The current distribution package is explicitly marked **not shippable** and must not be used as a public download.
- The open browser issue and other unfinished user paths must be resolved and covered by regression tests.
- Full post-integration regression and end-to-end verification are still required.
- Clean Windows packaging and manifest/content verification remain outstanding.
- Independent security review and legal review remain outstanding.
- The current build must not be treated as a substitute for a mature, independently reviewed password manager.

Please use synthetic test data only during development.

## Platform

- **Current target:** Windows 10/11, 64-bit.
- **Technology:** Flutter and Dart, with native Windows components where required.
- **Other platforms:** macOS, Linux, Android and iOS are not currently offered.

## Roadmap

Work is being organized around the following high-level priorities:

1. Reproduce the browser content-disappearance issue and identify its root cause across toolbar state, content rendering and related UI lifecycle paths.
2. Review neighboring browser workflows, fix verified defects and add regression coverage for affected states.
3. Continue completing the core vault workflows and validating data-protection boundaries.
4. Run the full integration and regression suite against the integrated application.
5. Produce a clean Windows package and verify its manifest and all included components.
6. Complete the outstanding security, legal and independent verification work.
7. Consider a public test build only after the applicable release gates have passed.

The roadmap is directional; it is not a delivery-date commitment. No release date is being announced.

## Project links

- **Product page:** [PySnake on NgocDolphin](https://ngocdolphincom.wordpress.com/pysnake/)
- **Vietnamese product page:** [PySnake — NgocDolphin (Tiếng Việt)](https://ngocdolphincom.wordpress.com/vi/pysnake/)
- **Publisher:** [NgocDolphin](https://ngocdolphincom.wordpress.com/)
- **Feedback and issue reports:** [GitHub Issues](https://github.com/ngocdolphin3275/PySnake/issues)


## Repository scope

This public repository is currently a **project-information page**. It contains the public product overview and status information; it does not publish the private application source code, development logs, test fixtures, vault data, build outputs or downloadable binaries.

---

<sub>PySnake · An independent NgocDolphin project · Public status updated 2026-11-21 · Latest documented development build: 0.1.0+12 (checkpoint: 2026-11-08)</sub>
