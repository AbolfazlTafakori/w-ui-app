# W-UI — Android app

The official Android client for [W-UI](https://github.com/AbolfazlTafakori/w-ui) panels.

- One tap to connect with your W-UI subscription — or with a single WireGuard, AmneziaWG or OpenVPN config, no subscription needed.
- Every protocol the panel offers: WireGuard, AmneziaWG, OpenVPN, and all W-UI stealth transports (veil, drift, relay, anchor, bare, mold, mirror).
- Servers with country flags, live latency, favorites, search and protocol filters.
- Import by link, by pasting a config, or by scanning a QR code (camera or a screenshot).
- English and Persian.

## Download

Get the latest version from **[Releases](https://github.com/AbolfazlTafakori/w-ui-app/releases/latest)**:

| File | For |
|---|---|
| `W-UI-x.y.z-arm64.apk` | Most phones (2017 and newer) |
| `W-UI-x.y.z-armv7.apk` | Older 32-bit phones |
| `W-UI-x.y.z-universal.apk` | Any phone, if unsure (larger) |

Android 8.0 or newer. Once installed, the app updates itself from **Settings → App update**: it downloads the right file for your phone, checks it against `SHA256SUMS` and its signature, then asks Android to install it.

### Verify a download

```bash
sha256sum -c SHA256SUMS --ignore-missing
```

---

## برنامه‌ی اندروید W-UI

کلاینت رسمی اندروید برای پنل‌های W-UI. با لینک اشتراک یا یک کانفیگ WireGuard، AmneziaWG یا OpenVPN با یک لمس وصل شوید. همه‌ی پروتکل‌ها و ترنسپورت‌های W-UI پشتیبانی می‌شوند.

آخرین نسخه را از بخش **Releases** دانلود کنید. برای بیشتر گوشی‌ها فایل `arm64` مناسب است؛ اگر مطمئن نیستید `universal` را بگیرید. بعد از نصب، برنامه از **تنظیمات ← به‌روزرسانی برنامه** خودش را به‌روز می‌کند و قبل از نصب، چک‌سام و امضای فایل را بررسی می‌کند.
