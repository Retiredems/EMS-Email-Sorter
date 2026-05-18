<p align="center">
  <img src="assets/icon.png" alt="EMS Email Sorter" width="96"/>
</p>

<h1 align="center">EMS Email Sorter</h1>

<p align="center">
  <strong>Sort Once. Send Smarter.</strong><br/>
  A professional desktop tool that classifies bulk email lists by mail provider — instantly, using live MX and SPF record lookups.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Lookup-MX%20%2F%20SPF-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Buckets-15%2B%20Providers-purple?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Commercial-orange?style=flat-square"/>
  <img src="https://img.shields.io/github/v/release/Retiredems/EMS-Email-Sorter?style=flat-square"/>
</p>

---

## What Is EMS Email Sorter?

EMS Email Sorter takes a raw list of email addresses and classifies every address into a named provider bucket — Office365, Gmail, Yahoo, AOL, GoDaddy, and 15+ others — by looking up each domain's MX and SPF DNS records in real time. The result is a clean set of per-provider output files ready to feed directly into your sending workflow.

Built for **email marketers**, **list managers**, and **bulk operators** who need to know exactly what they have before they send — on any Windows or macOS machine.

---

## Screenshots

<!-- Drop your screenshots in here -->

---

## Key Features

### Provider Classification
| Bucket | Mail Providers |
|--------|---------------|
| `office365.txt` | Microsoft 365 / Exchange Online |
| `gmail.txt` | Google Workspace / Gmail |
| `yahoo.txt` | Yahoo Mail |
| `aol.txt` | AOL Mail |
| `godaddy.txt` | GoDaddy Email Hosting |
| `rackspace.txt` | Rackspace Email |
| `qq.txt` | QQ Mail (Tencent) |
| `163.txt` / `126.txt` | NetEase Mail |
| `aliyun.txt` | Alibaba Cloud Mail |
| `263.txt` | 263 Enterprise Mail |
| `namecheap.txt` | Namecheap Private Email |
| `yandex.txt` | Yandex Mail |
| `mimecast.txt` | Mimecast Secure Email |
| `ionos.txt` | 1&1 / IONOS Mail |
| `others(mx).txt` | Unknown host — has MX records |
| `others(no_mx).txt` | No MX records found |

### Multi-Threaded Processing
- Configurable thread count for tuning speed vs. resource use
- Live progress with per-address status tracking
- Pause / resume mid-run without losing progress
- Per-domain isolation — one DNS failure never stalls the queue

### CSV-Aware
- Load `.txt` files (one email per line) or `.csv` files with any column layout
- The email column is auto-detected; all other columns are preserved unchanged
- Output files match your input format exactly — same columns, same order

### Output
- One result file per detected provider
- Unknown domains with MX records → `others(mx).txt`
- Domains with no MX → `others(no_mx).txt`
- Configurable output folder

### Premium Desktop UI
- Dark UI (default) with EMS-green accents
- Clean light theme — toggle from the toolbar
- Splash on launch, in-app activation, sidebar with cross-product links

---

## Installation

### Windows

1. Download `EMS-Email-Sorter-Setup.exe` from the [latest release](../../releases/latest)
2. Run the installer — follow the setup wizard
3. A desktop shortcut is created automatically
4. Enter your license key on first launch

> Installs per-user (no admin required). Works on any Windows 10 / 11 desktop, laptop, VPS, or RDP environment.

### macOS

1. Download `EMS_Email_Sorter_macOS.zip` from the [latest release](../../releases/latest)
2. Unzip and drag `EMS Email Sorter.app` to your Applications folder
3. Right-click → Open on first launch (Gatekeeper bypass for unsigned builds)
4. Enter your license key

---

## Getting a License

EMS Email Sorter is a **commercial product**. Licenses are hardware-tied — no cloud check-in required after activation.

👉 **Telegram: [@retiredems](https://t.me/retiredems)**
🤖 **Bot: [@emsmailerbot](https://t.me/emsmailerbot)**

**Pricing — single tier, lifetime only:**

| Plan | Price | Devices |
|------|-------|---------|
| Lifetime | **$100** | Up to 3 PCs |

No monthly. No yearly. One payment, three machines, forever.

---

## How to Get a License Key

1. Open EMS Email Sorter — your Hardware ID (HWID) is shown on the Activation screen
2. Tap **Copy** to copy the HWID
3. Open Telegram → [@emsmailerbot](https://t.me/emsmailerbot)
4. Select **📧 EMS Email Sorter** → submit your HWID and name
5. Complete payment → receive your key → paste it into the app

Your license is tied to your machine hardware. Up to **3 PCs per key** are accepted automatically. To move beyond that, contact [@retiredems](https://t.me/retiredems) for a transfer.

---

## Input Formats

### Plain Text List

A plain `.txt` file, one email address per line:

```
alice@example.com
bob@contoso.onmicrosoft.com
carol@gmail.com
dave@yahoo.com
```

Duplicates are removed before sorting begins.

### CSV File

Any `.csv` with an email column — the column is auto-detected:

```
Name,Email,Company
Alice,alice@example.com,Acme Corp
Bob,bob@contoso.onmicrosoft.com,Contoso
Carol,carol@gmail.com,Gmail User
```

Every output file contains all original columns in the same order.

---

## System Requirements

| | Windows | macOS |
|-|---------|-------|
| OS | Windows 10 / 11 (64-bit) | macOS 11+ (Intel or Apple Silicon) |
| RAM | 128 MB minimum | 128 MB minimum |
| Disk | 150 MB | 150 MB |
| Network | Required (DNS lookups) | Required (DNS lookups) |

> Outbound DNS (UDP/TCP port 53) is required for MX and SPF record lookups. No other outbound connection is needed.

---

## Changelog

### v1.0.0 — May 2026

- Initial public release
- MX/SPF classification into 15+ named provider buckets
- Multi-threaded DNS lookup worker pool, configurable per run
- Pause / resume without losing progress
- CSV input with full column preservation
- Unknown/no-MX fallback export
- Hardware-tied lifetime license — up to 3 PCs per key
- Dark / light theme, premium PyQt6 UI
- Splash screen on launch with in-app activation flow

---

## Other EMS Tools

| Tool | Description |
|------|-------------|
| [EMS Mailer](https://github.com/Retiredems/EMS-Mailer) | Bulk email sending — SMTP, rotating accounts, templates |
| [EMS Mail Fetcher](https://github.com/Retiredems/EMS-Mail-Fetcher) | Bulk IMAP / POP3 / OAuth account tester and email archiver |
| [EMS Country Sorter](https://github.com/Retiredems/EMS-Country-Sorter) | Sort bulk email lists by country — TLD + DNS + GeoIP detection |
| [EMS Cookie Harvester](https://github.com/Retiredems/EMS-Cookie-Harvester) | Extract email addresses from Office 365 session cookies via IMAP XOAUTH2 |
| [EMS Office365 Verifier](https://github.com/Retiredems/EMS-Office365-Verifier) | Classify Office 365 email lists by federation type |

---

## Support

Open an issue on GitHub for bug reports and feature requests. For licensing or transfers, message [@retiredems](https://t.me/retiredems) on Telegram.

---

<p align="center">
  Built with precision by <strong>Retiredems</strong> &nbsp;·&nbsp; Powered by PyQt6
</p>
