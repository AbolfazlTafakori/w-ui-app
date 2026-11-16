<p align="center"><img src="https://raw.githubusercontent.com/AbolfazlTafakori/w-ui/main/docs/public/logo.png" alt="W-UI" width="160"></p>
<h1 align="center">W-UI — Android &amp; Windows</h1>

<p align="center">
  The official client apps for <a href="https://github.com/AbolfazlTafakori/w-ui">W-UI</a> panels.
</p>

<p align="center">
  <a href="https://github.com/AbolfazlTafakori/w-ui-app/releases/latest"><img alt="Release" src="https://img.shields.io/github/v/release/AbolfazlTafakori/w-ui-app?color=e02e3d&label=release"></a>
  <img alt="Android" src="https://img.shields.io/badge/Android-8.0%2B-3DDC84?logo=android&logoColor=white">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white">
  <a href="https://abolfazltafakori.github.io/w-ui/guide/client-apps"><img alt="Docs" src="https://img.shields.io/badge/docs-client%20apps-blue"></a>
</p>

---

Add your W-UI subscription link once — paste it, or scan its QR code — and every server and protocol on it arrives in the app and stays current by itself: usage, expiry and new servers refresh on their own. A single WireGuard, AmneziaWG or OpenVPN file works too, with no subscription.

## Download

From **[Releases → latest](https://github.com/AbolfazlTafakori/w-ui-app/releases/latest)**:

| File | For |
|---|---|
| `W-UI-x.y.z-arm64.apk` | Android: most phones (2017 and newer) |
| `W-UI-x.y.z-armv7.apk` | Android: older 32-bit phones |
| `W-UI-x.y.z-universal.apk` | Android: any phone, if unsure (larger) |
| `W-UI-x.y.z-windows-setup.exe` | Windows 10 or 11, 64-bit |

- **Android 8.0 or newer.** Install the APK; Android may ask you to allow installing from your browser or file manager.
- **Windows:** run the setup. It asks for administrator rights once, to install the VPN service, then puts W-UI in the Start menu and on the desktop. Remove it from *Settings → Apps → Installed apps*.

Both apps update themselves from **Settings → App update**: they download the right file, check it against the release's `SHA256SUMS` (on Android also its signature), and only then install it.

### Verify a download

```bash
sha256sum -c SHA256SUMS --ignore-missing
```

On Windows (PowerShell): `Get-FileHash .\W-UI-x.y.z-windows-setup.exe` and compare with the line in `SHA256SUMS`.

## What it does

| | Android | Windows |
|---|---|---|
| WireGuard, AmneziaWG | ✓ | ✓ |
| OpenVPN | ✓ | ✓ |
| W-UI stealth transports: veil, drift, relay, anchor, bare, mold, mirror | ✓ | ✓ |
| IKEv2, L2TP/IPsec | ✓ | ✓ through Windows' own VPN |
| PPTP | — | ✓ through Windows' own VPN |
| OpenConnect (Cisco) | ✓ | — |
| Kill switch | ✓ | ✓ |
| Split tunnelling | by app | by destination, with Iran's addresses as a ready list |
| Real-delay test of every server, TCP ping | ✓ | ✓ |
| Select several servers: ping, test, favorite or delete together | ✓ | ✓ |
| QR scanner | camera | webcam, or a picture of the code |
| App lock | PIN and fingerprint | PIN |
| Share the VPN on the local network (SOCKS5/HTTP) | ✓ | ✓ |
| Languages | English, Persian | English, Persian |

Servers come with country flags, live latency, favorites, search and protocol filters. The stealth transports are what get through where plain VPN traffic is blocked; only the W-UI apps speak them.

## Privacy

The apps talk only to your W-UI panel (for the subscription), to the servers you connect to, and to GitHub (for app updates). No accounts, no analytics, no ads.

## Developer

Designed and developed by **Abolfazl Tafakori** — [github.com/AbolfazlTafakori](https://github.com/AbolfazlTafakori).

Built on open-source software: OpenVPN (GPLv2), amneziawg-go and wireguard-windows (MIT), Wintun, ZXing (Apache 2.0), flag-icons (MIT) and ip-location-db (CC0). The licences are listed in each app under *Settings → About*.

---

## برنامه‌های اندروید و ویندوز W-UI

کلاینت‌های رسمی پنل‌های [W-UI](https://github.com/AbolfazlTafakori/w-ui). لینک سابسکریپشن را یک بار اضافه کنید (با چسباندن یا اسکن QR آن) تا همهٔ سرورها و پروتکل‌ها بیایند و خودشان به‌روز بمانند. یک فایل تکی وایرگارد، AmneziaWG یا OpenVPN هم بدون سابسکریپشن کار می‌کند.

### دانلود

از **[آخرین نسخه در Releases](https://github.com/AbolfazlTafakori/w-ui-app/releases/latest)**:

- **اندروید (۸ به بالا):** برای بیشتر گوشی‌ها `arm64`، برای گوشی‌های قدیمی ۳۲ بیتی `armv7`، و اگر مطمئن نیستید `universal`.
- **ویندوز ۱۰ و ۱۱ (۶۴ بیتی):** فایل `W-UI-x.y.z-windows-setup.exe`. یک بار دسترسی مدیر می‌خواهد تا سرویس VPN را نصب کند، بعد W-UI در منوی استارت و روی دسکتاپ قرار می‌گیرد.

هر دو برنامه از **تنظیمات ← به‌روزرسانی برنامه** خودشان را به‌روز می‌کنند و قبل از نصب، فایل را با `SHA256SUMS` (و در اندروید با امضای آن) می‌سنجند.

### امکانات

وایرگارد، AmneziaWG، OpenVPN و همهٔ ترنسپورت‌های پنهان W-UI (veil، drift، relay، anchor، bare، mold، mirror) در هر دو؛ IKEv2 و L2TP در هر دو، PPTP در ویندوز و OpenConnect در اندروید. کیل‌سوییچ، تونل جداگانه (اندروید بر اساس برنامه، ویندوز بر اساس مقصد با فهرست آمادهٔ آدرس‌های ایران)، تست تأخیر واقعی، انتخاب چند سرور و انجام یک کار روی همه، اسکنر QR (دوربین یا وبکم)، قفل برنامه، اشتراک VPN در شبکهٔ محلی، فارسی و انگلیسی.

### سازنده

طراحی و توسعه: **ابوالفضل تفکری** — [github.com/AbolfazlTafakori](https://github.com/AbolfazlTafakori)
