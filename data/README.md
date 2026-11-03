# Data Pools (مخازن داده) — ARAL ULTRA

این پوشه شامل فهرست‌های عمومیِ داده است که «مخازن داده» پنل ARAL ULTRA را تغذیه می‌کنند:
چرخش خودکار IP تمیز، ساخت سریع لوکیشن‌های خروجی و تعویض خودکار پروکسی خراب.

This folder holds public, community-maintained data lists that feed the ARAL ULTRA
panel's Data Pools: per-user clean-IP auto-rotation, quick exit-location creation
and broken-proxy auto-replacement.

## Files / فایل‌ها

| File | Purpose | مصرف در پنل |
| --- | --- | --- |
| `ips.txt` | Clean IPv4 addresses (one per line) | چرخش IP تمیز IPv4 |
| `ip6.txt` | Clean IPv6 addresses | چرخش IP تمیز IPv6 |
| `dom.txt` | Clean domains | چرخش دامنهٔ تمیز |
| `ech-dom.txt` | Domains supporting ECH | سازندهٔ ECH |
| `ech-dns.txt` | DoH resolvers for ECH combos | سازندهٔ ECH |
| `proxy/<CC>.txt` | Public exit proxies per country (plain `socks5://ip:port` / `http://`) | لوکیشن‌های خروجی |
| `proxy_vip/<CC>.txt` | Curated (VIP) public proxies per country | لوکیشن‌های خروجی منتخب |
| `vip-list.json` | Country manifest for `proxy_vip/` | فهرست کشورهای VIP |

## How to use / نحوهٔ استفاده

1. **سریع‌ترین راه — آپلود در پنل:** متن هر فایل را کپی و در
   `شبکه و Fragment → مخازن داده` بچسبانید و «ذخیرهٔ مخزن» بزنید (ذخیره در KV).
2. **خودکار از گیت‌هاب:** این پوشه را در یک ریپوی GitHub خودتان منتشر کنید و در
   همان بخش، نام ریپو (`owner/repo`) را وارد و «دریافت از گیت‌هاب» را بزنید.
   پنل به‌صورت خودکار `data/…` را هر ساعت تازه‌سازی می‌کند.

> نکته: این فهرست‌ها دادهٔ عمومی و «واقعی» هستند (آدرس IP و اندپوینت‌های عمومی) و
> بدون اعتبارنامه منتشر شده‌اند. کیفیتِ پروکسی‌های عمومی متغیر است؛ پنل به‌صورت
> خودکار موارد سالم را جایگزین می‌کند.
