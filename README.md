<div align="center">

# ARAL ULTRA · V4.1 — OBSIDIAN & GOLD · ULTRA EDITION

**پنل آزاد و رایگانِ مدیریت اشتراک VLESS، Trojan و Shadowsocks و پروکسی رسمی تلگرام روی شبکهٔ ابری کلادفلر — به‌هم‌پیوستهٔ دو نسل پنل، با قوی‌ترین قابلیت‌ها**
*Free Serverless VLESS, Trojan & Shadowsocks, Fragment/Pattern/ECH anti-DPI, Multi-Location Exits & Official Telegram Web Proxy Panel on Cloudflare Workers & Pages*

![Version](https://img.shields.io/badge/Version-4.1.0_ULTRA-d4af37?style=flat-square) ![Runtime](https://img.shields.io/badge/Cloudflare-Workers%20%26%20Pages-0c0b09?style=flat-square) ![Theme](https://img.shields.io/badge/Theme-Obsidian%20%26%20Gold-8a6a14?style=flat-square)

[کانال رسمی / Official Channel — Telegram](https://t.me/AralDev)

</div>

---

> ### اطلاعیه (رایگان و غیرقابل فروش)
> **ARAL ULTRA** نرم‌افزار آزاد و رایگان است؛ خرید و فروش سورس، پنل یا لینک اشتراکِ ساخته‌شده با آن مجاز نیست.
> **ARAL ULTRA is free software — strictly not for sale.**

---

## ویژگی‌ها / Features

### هستهٔ تونل / Core
- **VLESS + Trojan + Shadowsocks روی WebSocket** — سه پروتکل همزمان؛ رمز ss به‌صورت خودکار از UUID ساخته می‌شود
  *VLESS + Trojan + Shadowsocks over WS — all three protocols, ss secrets auto-derived from the UUID*
- **Fragment (۱-۱ / tlshello) + Pattern JSON (fm) + Cipher Suites (cs) + TLS Mask** ضد DPI
  *Anti-DPI: fragment + advanced pattern JSON + custom cipher suites + TLS masking*
- **ECH (Encrypted Client Hello)** — سازندهٔ ترکیب‌های `dom+udp/tcp/https://dns`
  *ECH combo builder (UDP / TCP / DoH)*
- **اثر انگشت TLS** به انتخاب: chrome, firefox, safari, ios, android, edge, 360, qq, random, randomized, unsafe
  *Selectable uTLS fingerprint per subscriber*
- **ProxyIP · NAT64 · زنجیرهٔ SOCKS5/HTTP/SOCKS4** برای رفع بلاک و خروج چندلایه
  *ProxyIP, NAT64 and multi-hop chain proxy fallbacks*

### قابلیت‌های ULTRA / Ultra Features
- **لوکیشن‌های خروجی چندگانه (تا ۱۵ لوکیشن)** برای هر مشترک — هر لوکیشن یک مسیر `/loc-N` و یک گروه مستقل در اشتراک با پرچم کشور
  *Up to 15 per-user exit locations, each a `/loc-N` node group with country flags*
- **تعویض خودکار پروکسی خراب** از مخازن داده، با حفظ کشورِ همان لوکیشن
  *Broken-exit auto-replacement from data pools, country-preserving*
- **چرخش خودکار IP تمیز** برای هر مشترک (ترکیب IPv4/IPv6/دامنه، تعداد قابل تنظیم، هر بار دریافت اشتراک تازه می‌شود)
  *Per-user clean-IP auto-rotation (mixed v4/v6/domains) on every subscription fetch*
- **سهمیهٔ تعداد اتصال (Request Quota) و حد دستگاه همزمان (IP Limit)** — با اعمال واقعی روی خط
  *Request quota + concurrent-device limits — actually enforced on the tunnel*
- **ریست خودکار حجم/سهمیه هر N روز** و **شروع اعتبار از اولین اتصال**
  *Auto-reset schedules and start-on-first-connect*
- **مسدودسازی بزرگسال/تبلیغات** به‌ازای هر مشترک با DoH خانواده + تشخیص غیرفعالِ SNI (fail-open)
  *Per-user adult/ads blocking via family DoH + passive SNI sniffing (fail-open)*
- **عملیات گروهی**: انتخاب چندتایی، فعال/غیرفعال‌سازی، ریست حجم/سهمیه/زمان و حذف گروهی
  *Bulk operations: multi-select enable/disable/reset/delete*
- **مخازن داده (Pools)**: IP تمیز و پروکسی عمومی — آپلود مستقیم در KV یا دریافت خودکار از مخزن GitHub خودتان
  *Data pools: paste into KV or auto-fetch from your own GitHub repo (`data/` folder)*
- **پیش‌تنظیم‌های اپراتوری ایران**: همراه اول، ایرانسل، رایتل، مخابرات و گیمینگ — یک‌ضرب روی هر مشترک
  *Iranian ISP fragmentation presets (MCI / Irancell / Rightel / TCI / Gaming) per subscriber*

### افزوده‌های نسخهٔ ۴.۱ / What's New in v4.1
- **اعمال قوانین در میانهٔ اتصال (Heartbeat)** — هر ~۲۲ ثانیه وضعیت مشترک بازبینی می‌شود؛ اتمام حجم/سهمیه، انقضا، توقف یا حذف، تونلِ زنده را بلافاصله قطع می‌کند
  *Mid-connection enforcement heartbeat (~22s): quota/expiry/pause/deletion kills live tunnels instantly*
- **حسابداری عمر و مشترکین حذف‌شده** — مصرفِ کلِّ عمر هر مشترک هرگز ریست نمی‌شود و با حذف مشترک به حساب سرور منتقل می‌شود
  *Lifetime (never-reset) per-user accounting + deleted-subscriber traffic preserved in server totals*
- **پورت‌های اختصاصی هر مشترک** و **نوع مخزن چرخش** (فقط IPv4 / IPv6 / دامنه / ترکیبی)
  *Per-user port overrides + rotation pool type (IPv4 / IPv6 / domains / mixed)*
- **زمان‌بندی جداگانهٔ ریست سهمیهٔ اتصال** مستقل از ریست حجم
  *Independent request-quota auto-reset schedule, separate from volume resets*
- **پرکردن هوشمند لوکیشن‌ها** — نمونه‌گیری از مخزن پروکسی، آزمودن زنده و انتخاب ۵ خروجی سالم با کم‌ترین پینگ (بدون تکرار کشور)
  *Smart location fill: sample the proxy pool, live-probe, and auto-fill the 5 healthiest exits*
- **بروزرسانی خودکار هسته** (اختیاری) — هر ۵ دقیقه بررسی و نصب بی‌دخالتِ نسخهٔ جدید از مخزن رسمی
  *Optional hands-free core auto-update (5-minute checks against the official repo)*
- **ری‌استارت هسته** — تخلیهٔ امن کش‌های حافظه با حفظ کامل حسابداری ترافیک
  *Restart-core: safe in-memory cache flush with zero accounting loss*
- **بازیابی رمز با توکن کلادفلر** — اثبات مالکیت ورکر و بازگشت به فرم تعیین رمز، بدون از دست رفتن مشترکین
  *Cloudflare-token password recovery — ownership proof that preserves every subscriber*
- **بروزرسانی زندهٔ دفتر مشترکین** (۵ث تا ۵دق قابل تنظیم) و **نام مستعار `/feed/`** برای اشتراک
  *Live users-ledger auto-refresh (5s–5m) and the `/feed/` subscription alias*

### پنل و اشتراک / Panel & Subscriptions
- **اشتراک هوشمند چندقالبی** — Base64، Xray JSON، Sing-box، Clash/Mihomo + صفحهٔ «کارت مشترک» زنده با نوارهای مصرف/اعتبار/سهمیه و QR
  *Multi-format subscriptions (Base64 / Xray / Sing-box / Clash) + live status page with progress bars & QR*
- **پروکسی رسمی تلگرام** (`tg://webproxy`) بدون برنامهٔ جانبی + **DoH خصوصی** برای هر مشترک
  *Official Telegram Web Proxy + per-subscriber Private DoH*
- **نوسان‌نگار زنده** پینگ/سرعت، اسکنر IP تمیز با رنج‌های رسمی کلادفلر و مشاور هوشمند ISP
  *Live RTT/speed telemetry, clean-IP scanner with official CF ranges, smart ISP advisor*
- **PWA** — نصب‌شدن به‌عنوان اپلیکیشن روی موبایل و دسکتاپ
  *Installable Progressive Web App*
- **تم Obsidian & Gold** با حالت دارک/لایت، دوزبانه (فارسی/انگلیسی) و بدون هیچ لوگوی تصویری
  *Obsidian & Gold theme, dark/light, bilingual FA/EN — deliberately logo-free (wordmark only)*
- **پشتیبان‌گیری/بازیابی JSON**، مانیتور سهمیهٔ روزانهٔ کلادفلر و **بروزرسانی هسته از گیت‌هاب**
  *JSON backup/restore, CF daily-quota monitor, GitHub core self-updater*
- **امنیت**: PBKDF2-SHA256، نشست امضاشدهٔ HMAC، محدودسازی تلاش ناموفق ورود
  *PBKDF2-HMAC sessions, login throttling*

## تایپوگرافی و هویت / Typography & Identity

| نقش | فونت |
| --- | --- |
| تیترها / Headings | **DM Serif Display** |
| متن لاتین / Body (latin) | **Bodoni Moda** |
| فارسی / Farsi | **Vazirmatn** |
| کد و اعداد فنی / Mono | **JetBrains Mono** |

نسخهٔ ULTRA عمداً **بدون لوگو** منتشر می‌شود؛ هویت فقط با واترمارک متنی `Aral Ultra` در نام نودها و سربرگ پنل حفظ می‌شود.
*The ULTRA edition is deliberately logo-free — the `Aral Ultra` text watermark lives in the masthead and node remarks.*

## استقرار سریع — Workers / Quick Deploy (Workers)

1. در کلادفلر یک **KV namespace** با نام `aral` بساز.
2. یک Worker جدید بساز (Hello World) و کل محتوای `worker-single-file.js` را در **Edit code** جای‌گذاری و **Deploy** کن.
3. از **Settings → Bindings → KV namespace** متغیر `KV` را به فضای `aral` وصل کن.
4. صفحهٔ پنل را باز کن — فرم انتخاب رمز مدیر ظاهر می‌شود.

*Full English steps are rendered inside the panel itself (stateless view).*

## استقرار — Pages / Deploy (Pages)

پوشهٔ `dist/` (شامل `index.html` و `_worker.js`) یا بستهٔ آمادهٔ `aral-ultra-pages.zip` را در **Workers & Pages → Create → Pages → Upload assets** آپلود کن.

## توسعهٔ محلی / Local Development

```bash
npm install          # نصب وابستگی‌ها / install dependencies
npm run build        # ساخت worker-single-file.js + panel-preview.html + dist/
npm run dev          # اجرای محلی با wrangler
npm test             # تست E2E با playwright (17/17)
```

## مخازن داده / Data Pools

پوشهٔ `data/` شامل فهرست‌های عمومیِ IP تمیز و پروکسی‌های خروجی است. برای فعال‌سازی چرخش IP و لوکیشن‌های آماده، متن فایل‌ها را در پنل (`شبکه و Fragment → مخازن داده`) ذخیره کن یا این پوشه را در یک ریپوی GitHub خودت منتشر و در پنل `owner/repo` را ثبت کن. جزئیات: `data/README.md`.

*The bundled `data/` folder feeds clean-IP rotation and exit locations — upload it via the panel or point the panel at your own GitHub repo.*

## اسکریپت‌های جانبی / Side Scripts

- `aral-relay.sh` — نصب‌کنندهٔ ریلی SOCKS5 (GOST + systemd) برای سرور شخصی؛ خروجی را مستقیم در «لوکیشن‌های خروجی» مشترک بگذار.
  *SOCKS5 relay builder for your own VPS — paste the output as a subscriber location.*
- `aral-scanner.txt` — اسکنر چندگانه (مرورگر/پایتون/پاورشل) برای یافتن IP تمیز با SNI دامنهٔ خودت.
  *Polyglot SNI clean-IP scanner (browser / Python / PowerShell).*

## بروزرسانی هسته / Core Self-Updater

پنل به‌صورت پیش‌فرض نسخهٔ جدید را از مخزن `AralDev/Aral` بررسی می‌کند (نسخهٔ ۴ ULTRA بالاتر از ۳.x رسمی است و پیشنهادِ پایین‌آوردن نمی‌گیرد). اگر مخزن شخصی خودت را می‌خواهی، ثابت‌های `GITHUB_REPO` را در `src/storage.js` و `OFFICIAL_GITHUB_REPO` را در `src/ui/app.js` تغییر بده.

*The updater checks `AralDev/Aral` (branch `main`) — point those two constants at your own fork if needed.*

## ساختار مخزن / Repository Layout

```
├─ build.mjs               # پایپ‌لاین ساخت (فونت‌سابی، فشرده‌سازی، استلث، ممیزی امضا)
├─ worker-single-file.js   # خروجی نهایی برای Workers
├─ aral-ultra-pages.zip    # بستهٔ آمادهٔ Pages
├─ wrangler.toml / config.json
├─ aral-relay.sh           # نصب‌کنندهٔ ریلی SOCKS5
├─ aral-scanner.txt        # اسکنر چندگانهٔ SNI
├─ data/                   # مخازن داده (IP تمیز، دامنه، پروکسی‌های عمومی، ECH)
├─ src/
│  ├─ worker.js            # ورودی Worker (API + مسیریابی + PWA)
│  ├─ sub.js               # مولد اشتراک و کارت مشترک (لوکیشن‌ها، fm/cs/mask/ECH)
│  ├─ protocols.js         # موتور تونل VLESS/Trojan/ss + سهمیه‌ها + DoH
│  ├─ sslib.js             # موتور Shadowsocks AEAD + اسنiffer و مسدودساز
│  ├─ pools.js / poolutil.js # لایهٔ مخازن داده
│  ├─ tgproxy.js           # پروکسی رسمی تلگرام
│  ├─ storage.js           # لایهٔ KV و ثابت‌های برند
│  ├─ crypto.js            # توابع رمزنگاری
│  └─ ui/                  # رابط کاربری (HTML/CSS/JS + فونت‌ها)
└─ assets/                 # وکتور تم (بدون لوگو)
```

---

<div align="center">

**ARAL ULTRA V4.1 · OBSIDIAN & GOLD** · [t.me/AralDev](https://t.me/AralDev) · FREE · NOT FOR SALE

</div>

---

> ### یادداشت استفادهٔ مسئولانه / Responsible-Use Notice
> این بستهٔ «ادغام‌شده» صرفاً برای **استفادهٔ شخصی و آموزشی** تهیه شده است. اجزای مقدماتی آن از پروژه‌های عمومی برداشته و بازنویسی شده‌اند؛ لطفاً نتیجه را بازنشر، فروش یا میزبانی عمومی نکن و قوانین پلتفرم‌های میزبان (کلادفلر/گیت‌هاب) و قوانین محلی را رعایت کن.
> *This merged bundle is prepared strictly for **personal, educational use**. Its building blocks were adapted from public projects — do not redistribute, sell, or publicly host the result, and respect the terms of your hosting platforms and local laws.*

</div>
