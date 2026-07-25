<div align="center" dir="rtl">

<img src="https://raw.githubusercontent.com/Xknohub/Frei/main/brand/frei-logo-badge-round.png" width="70" alt="Frei">

<div align="left">
  <a href="README.md">🇬🇧 English</a>
</div>

# 🌟 فری پروکسی (Frei Proxy)

**یک پروکسی شخصی و ضدسانسور به‌همراه پنل مدیریت، روی یک Cloudflare Worker.**

VLESS · Trojan · Shadowsocks · gRPC · XHTTP روی WebSocket + TLS — با پنل دوم‌زبانه
(English + فارسی)، بهینه‌سازی IP تمیز به‌تفکیک ISP، حساب چندکاربره، ربات تلگرام،
WARP، زنجیره پروکسی و حالت Backend. اجرا روی **پلن رایگان** Cloudflare.

[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/نسخه-3.6.3-blueviolet?style=for-the-badge)](https://github.com/Xknohub/Frei)
[![Stars](https://img.shields.io/github/stars/Xknohub/Frei?style=for-the-badge&color=0ea5e9)](https://github.com/Xknohub/Frei)

</div>

---

## 🌐 لینک‌ها

<div align="center">

[![Website](https://img.shields.io/badge/🌐%20سایت-freiproxy.online-0ea5e9?style=for-the-badge)](https://freiproxy.online/)
[![Telegram Channel](https://img.shields.io/badge/✈️%20کانال%20تلگرام-@frei__proxy-0ea5e9?style=for-the-badge&logo=telegram)](https://t.me/freir_proxy)
[![Telegram Group](https://img.shields.io/badge/👥%20گروه%20تلگرام-@freiproxy__group-0ea5e9?style=for-the-badge&logo=telegram)](https://t.me/freiproxy_group)
[![YouTube](https://img.shields.io/badge/▶️%20یوتیوب-@freiproxyir-ff0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@freiproxyir)
[![X (Twitter)](https://img.shields.io/badge/𝕏%20شبکه%20ایکس-@FreiProxy-000000?style=for-the-badge&logo=x)](https://x.com/FreiProxy)
[![Instagram](https://img.shields.io/badge/📸%20اینستاگرام-@frei__proxy-E4405F?style=for-the-badge&logo=instagram)](https://www.instagram.com/freir_proxy)

</div>

---

## 📖 فری پروکسی چیست؟

فری یک **پروکسی شخصی و همه‌کاره برای دور زدن سانسور** است که کاملاً روی Cloudflare Workers — **پلن رایگان** — اجرا می‌شود. این پروژه یک پروکسی قدرتمند (VLESS، Trojan، Shadowsocks روی WebSocket/gRPC/XHTTP) را با **پنل مدیریت کامل دوم‌زبانه** در یک Worker واحد ترکیب کرده است.

**چیزهایی که فری را متفاوت می‌کند:**
- ⚡ **بدون نیاز به زیرساخت** — بدون VPS، بدون دامنه برای شروع
- 🌍 **IP تمیز به‌تفکیک ISP** — بهینه‌سازی خودکار برای هر اپراتور ایرانی
- 👥 **چندکاربره** — لینک اختصاصی با سهمیه، تاریخ انقضا و کنترل روشن/خاموش
- 🤖 **ربات تلگرام** — مدیریت کامل از طریق تلگرام
- 🔗 **زنجیره پروکسی** — SOCKS5، HTTP، HTTPS، TURN، SSTP
- 🛡️ **دورزدن پیشرفته** — ECH، TLS fragment، 0-RTT، fingerprint
- 🧩 **حالت Backend** — اتصال به VPS شخصی Xray/sing-box برای VLESS + تماس تصویری

---

## ⚡ نصب سریع

روش مورد نظر خود را انتخاب کنید:

### 🖥️ Frei Wizard (دسکتاپ)

نرم‌افزار رسمی دسکتاپ با رابط گرافیکی — بدون نیاز به دانش فنی.

[**→ دانلود Frei Wizard برای ویندوز و لینوکس**](https://github.com/Xknohub/Frei-Wizard)

### 🌐 نصب از طریق سایت

به سایت رسمی مراجعه کرده و مراحل گام‌به‌گام را دنبال کنید:

[**→ freiproxy.online/install**](https://freiproxy.online/install)

---

### 📱 موبایل

- **Android:** **رادار** با ویزارد داخلی برای نصب آسان فری روی کلودفلر — به‌زودی منتشر می‌شود.
- **iOS:** در دست توسعه.

---

## 🛰 حالت Backend (VLESS + تماس تصویری/صوتی)

Cloudflare Workers نمی‌تواند پروکسی TCP بومی اجرا کند یا ترافیک UDP را مستقیماً مدیریت کند. برای فعال‌سازی این قابلیت‌ها، فری از **حالت Backend** پشتیبانی می‌کند — ارسال ترافیک به VPS شخصی Xray یا sing-box.

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/Xknohub/Frei/main/nova-backend.sh)
```

پس از اجرای نصاب، حالت Backend را در پنل فری فعال کنید (تنظیمات شبکه → حالت Backend) و آدرس VPS خود را وارد کنید.

---

## 📋 پیش‌نیازها

- یک **حساب Cloudflare** (رایگان) با Workers فعال
- یک **فضای KV** (با دیپلوی یک‌کلیکی خودکار ساخته می‌شود، یا دستی با Wrangler)
- (اختیاری) Node.js v18+ و Wrangler CLI برای تست محلی

---

## 🧬 تفاوت نسخه‌ها (v1 → v2 → v3)

| قابلیت / Feature | v1 | v2 | v3 |
|-----------------|:---:|:---:|:---:|
| دریافت لینک اشتراک خودکار | ✅ | ✅ | ✅ |
| فرمت Base64 | ✅ | ✅ | ✅ |
| Clash / Mihomo | ✅ | ✅ | ✅ |
| sing-box | ✅ | ✅ | ✅ |
| Loon | ✅ | ✅ | ✅ |
| Surge | ✅ | ✅ | ✅ |
| توزیع بار | ✅ | ✅ | ✅ |
| بررسی سلامت | ✅ | ✅ | ✅ |
| تست پینگ | ✅ | ✅ | ✅ |
| بهترین کانفیگ | ✅ | ✅ | ✅ |
| QR Code | ✅ | ✅ | ✅ |
| نمایش لیست کانفیگ | ✅ | ✅ | ✅ |
| پروکسی DoH | ✅ | ✅ | ✅ |
| رمزگذاری DNS | ✅ | ✅ | ✅ |
| Load Balance / Failover / Caching DNS | ✅ | ✅ | ✅ |
| DNS محلی | ✅ | ✅ | ✅ |
| دور زدن تحریم DNS | ✅ | ✅ | ✅ |
| IP جعلی / Fake DNS | ✅ | ✅ | ✅ |
| مسیریابی / GeoIP / GeoSite | ✅ | ✅ | ✅ |
| اتصال مستقیم به سایت ایرانی | ✅ | ✅ | ✅ |
| پشتیبانی IPv6 | ✅ | ✅ | ✅ |
| مسدودسازی تبلیغات و بزرگسال | ✅ | ✅ | ✅ |
| پورت‌های کلادفلیر | ✅ | ✅ | ✅ |
| لینک مستقیم Trojan | ✅ | ✅ | ✅ |
| لینک مستقیم Clash | ✅ | ✅ | ✅ |
| حالت سراسری SOCKS5 | ✅ | ✅ | ✅ |
| حالت سراسری HTTP | ✅ | ✅ | ✅ |
| اسکن IP تمیز | ✅ | ✅ | ✅ |
| نوتیفیکیشن تلگرام | ✅ | ✅ | ✅ |
| مدیریت ربات تلگرام | ✅ | ✅ | ✅ |
| Quantumult X | ➖ | ✅ | ✅ |
| تشخیص خودکار کلاینت | ➖ | ✅ | ✅ |
| Random Path / Wildcard Host | ➖ | ✅ | ✅ |
| پنل مدیریت فارسی (RTL) | ➖ | ✅ | ✅ |
| حالت ساده و پیشرفته | ➖ | ✅ | ✅ |
| تم تاریک | ➖ | ✅ | ✅ |
| ویرایشگر JSON | ➖ | ✅ | ✅ |
| مشاهده لاگ | ➖ | ✅ | ✅ |
| بازنشانی تنظیمات | ➖ | ✅ | ✅ |
| VLESS + Trojan + Shadowsocks | ➖ | ✅ | ✅ |
| gRPC + XHTTP transport | ➖ | ✅ | ✅ |
| WebSocket Early Data | ➖ | ✅ | ✅ |
| mux=0 برای Shadowsocks | ➖ | ✅ | ✅ |
| زنجیره SOCKS5 | ➖ | ✅ | ✅ |
| زنجیره HTTP/HTTPS CONNECT | ➖ | ✅ | ✅ |
| زنجیره TURN + SSTP | ➖ | ✅ | ✅ |
| حالت سراسری HTTPS / TURN / SSTP | ➖ | ✅ | ✅ |
| لیست سفید دامنه | ➖ | ✅ | ✅ |
| زنجیره در لینک اشتراک | ➖ | ✅ | ✅ |
| TLS 1.3 / 1.2 | ➖ | ✅ | ✅ |
| ChaCha20-Poly1305 / AES-GCM | ➖ | ✅ | ✅ |
| ClientHello سفارشی / ALPN | ➖ | ✅ | ✅ |
| SNI fragment / TLS fragment | ➖ | ✅ | ✅ |
| بازگشت به ChaCha20 | ➖ | ✅ | ✅ |
| AES-128/256-GCM (Shadowsocks) | ➖ | ✅ | ✅ |
| تشخیص خودکار / کلید جلسه پویا | ➖ | ✅ | ✅ |
| بهینه‌سازی آنلاین / API / لیست IP دلخواه | ➖ | ✅ | ✅ |
| تولید IP تصادفی / دسته‌بندی نتایج | ➖ | ✅ | ✅ |
| ذخیره و جایگزینی نتایج | ➖ | ✅ | ✅ |
| بهینه‌سازی IP به‌تفکیک ISP | ➖ | ✅ | ✅ |
| Webhook تلگرام / تنظیمات ربات در پنل | ➖ | ✅ | ✅ |
| مشاهده مصرف Cloudflare / API Token | ➖ | ✅ | ✅ |
| API مصرف سفارشی | ➖ | ✅ | ✅ |
| لینک مستقیم VLESS + Shadowsocks | ➖ | ✅ | ✅ |
| اشتراک با توکن | ➖ | ✅ | ✅ |
| کپی یک‌کلیک | ➖ | ✅ | ✅ |
| فضای KV (Config, CF, TG, IPs, Logs) | ➖ | ✅ | ✅ |
| ورود با رمز / Auth Cookie | ➖ | ✅ | ✅ |
| اعتبارسنجی UUID / Token Auth (MD5) | ➖ | ✅ | ✅ |
| مسدودسازی speed test | ➖ | ✅ | ✅ |
| متغیرهای محیطی | ➖ | ✅ | ✅ |
| پنل واکنش‌گرا فارسی / Persian RTL responsive | ➖ | ✅ | ✅ |
| نقشه Leaflet / Toast / Modal | ➖ | ✅ | ✅ |
| ماژول‌های جمع‌شونده / SVG icons | ➖ | ✅ | ✅ |
| کپی به کلیپ‌بورد | ➖ | ✅ | ✅ |
| TCP همزمان / 0-RTT | ➖ | ✅ | ✅ |
| تجمیع آپلود / داونلود | ➖ | ✅ | ✅ |
| محدودیت صف آپلود | ➖ | ✅ | ✅ |
| Load Balance IP / Proxy Fallback | ➖ | ✅ | ✅ |
| لینک اشتراک بدون توکن با فرمت نام‌گذاری شده | ➖ | ➖ | ✅ |
| آینه دائمی گیتهاب برای اشتراک | ➖ | ➖ | ✅ |
| پنل یکپارچه (Static Assets) | ➖ | ➖ | ✅ |
| رابط کاربری دوم‌زبانه + تور راهنما | ➖ | ➖ | ✅ |
| مسدودسازی بدافزار / فیشینگ / Cryptominers | ➖ | ➖ | ✅ |
| مسدودسازی QUIC | ➖ | ➖ | ✅ |
| حالت Backend (VLESS + UDP / تماس تصویری) | ➖ | ➖ | ✅ |
| ECH (رمزنگاری SNI) | ➖ | ➖ | ✅ |
| Port-spread / Multi-transport | ➖ | ➖ | ✅ |
| اعلام خودکار به‌روزرسانی دامنه در تلگرام | ➖ | ➖ | ✅ |
| نمودار ترافیک روزانه + تفکیک آپلود/دانلود | ➖ | ➖ | ✅ |
| لینک اختصاصی کاربر + سهمیه کل/روزانه + انقضا + روشن/خاموش + غیرفعال خودکار | ➖ | ➖ | ✅ |
| لینک اشتراک کاربر با نام کاربری + کلید مخفی | ➖ | ➖ | ✅ |
| کش خواندن-پس-از-نوشتن KV برای انتشار آنی تنظیمات | ➖ | ➖ | ✅ |
| پشتیبانی NAT64 / انتقال IPv6 | ➖ | ➖ | ✅ |
| تغییر رمز پنل + ۲ مرحله‌ای (TOTP) + کد بازیابی | ➖ | ➖ | ✅ |
| محدودیت تلاش ورود + مدیریت نشست | ➖ | ➖ | ✅ |
| ثبت حساب WARP + لایسنس WARP+ + WoW | ➖ | ➖ | ✅ |
| تغییر endpoint WARP + نقاط ایران | ➖ | ➖ | ✅ |
| حالت Amnezia WARP + WARP Noise | ➖ | ➖ | ✅ |
| حالت یک‌کلیک ایران + گزارش زنده کانفیگ | ➖ | ➖ | ✅ |
| پشتیبان‌گیری و بازیابی کامل تنظیمات | ➖ | ➖ | ✅ |
| بازگشت میان‌افزاری (گره‌های غیر Cloudflare) | ➖ | ➖ | ✅ |
| استخر دامنه خودترمیم + بررسی سلامت | ➖ | ➖ | ✅ |
| عبور از کشورها (چین، روسیه، تحریم‌ها) | ➖ | ➖ | ✅ |
| قوانین مسیریابی سفارشی | ➖ | ➖ | ✅ |
| API مدیریت متمرکز + آمار ناوگان + اعلان همگانی | ➖ | ➖ | ✅ |
| خاموش کن سراسری (Kill switch) | ➖ | ➖ | ✅ |
| ضربان قلب نمونه + سامانه اعلان‌ها | ➖ | ➖ | ✅ |
| پایگاه داده D1 (انتقال از KV) | ➖ | ➖ | ✅ |
| ویزارد نصب /install + دیپلوی یک‌کلیکی | ➖ | ➖ | ✅ |

---

## 💜 حمایت از پروژه

اگر فری برایتان مفید بود، لطفاً با یک **⭐ ستاره** و یک دونیت کوچک از ادامه‌ی کار حمایت کنید.

<div align="center">

### ⭐ [به فری در گیتهاب ستاره بدهید](https://github.com/Xknohub/Frei) ⭐

[![Star on GitHub](https://img.shields.io/github/stars/Xknohub/Frei?style=for-the-badge&logo=github&label=Star%20Frei&color=8957e5)](https://github.com/Xknohub/Frei)

| ارز دیجیتال | آدرس |
|-------------|------|
| **TON** | `UQD51lGC35rP_SbVYgbFA7CEEii4GVMFgqj4N8fiGi6m425w` |

</div>

---

## 🙏 تشکر

ساخته شده با ❤️ برای اینترنت آزاد و باز.

- [@Xknohub](https://github.com/Xknohub) — سازنده
- [Cloudflare Workers](https://workers.cloudflare.com/)
- [Xray-core](https://github.com/XTLS/xray-core)

---

## 📜 شرایط: رایگان است و برای فروش نیست

**کد** فری متن‌باز و تحت مجوز MIT است: آزادی که خودت میزبانی کنی، مطالعه و تغییرش بدهی. فری یک **سرویس رایگان** است، پس شرایط زیر برای نام فری و کانفیگ‌هایی که می‌سازد اعمال می‌شود:

- **نفروش.** کانفیگ‌ها، اشتراک‌ها یا دسترسی فری را به‌عنوان محصول پولی نفروش. فری برای همه رایگان است.
- **نشان سرویس رایگان را حذف نکن.** هر نودِ ساخته‌شده یک نشان قفل‌شدهٔ `سرویس رایگان فری @freir_proxy` دارد. حذف آن برای جا زدن کانفیگ‌ها به‌عنوان سرویس پولی خودت مجاز نیست.
- **اعتبار را نگه دار.** اگر فورک یا بازتوزیع می‌کنی، اعتبار فری پروکسی و لینک به این ریپازیتوری را نگه دار.
- **جعل هویت نکن.** از نام، لوگو یا کانال فری برای جا زدن یک نسخهٔ ری‌برندشده به‌عنوان فری رسمی استفاده نکن.

مجوز MIT شامل کد می‌شود. نام، برند فری و وعدهٔ «رایگان ماندن» متعلق به پروژه است.

---

## مجوز

MIT — فایل [LICENSE](LICENSE) را ببینید. مجوز MIT برای سورس‌کد است؛ شرایط برند بالا برای نام و سرویس فری اعمال می‌شود.

---

<div align="center">

ساخته شده برای ایران <img src="https://raw.githubusercontent.com/Xknohub/Frei/main/flag-iran.svg" height="16" alt="Iran (Lion and Sun)" /> — و هرکس که به اینترنت آزاد نیاز دارد.
**هیچ اطلاعاتی از ترافیک شما ذخیره نمی‌شود. پروکسی متعلق به خود شماست.**

📖 [نسخه انگلیسی / English version](README.md)

---

<a href="https://www.star-history.com/?repos=Xknohub%2FFrei&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=Xknohub/Frei&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=Xknohub/Frei&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=Xknohub/Frei&type=date&legend=top-left" />
 </picture>
</a>

</div>

---

<div align="center">

ساخته شده توسط <a href="https://github.com/Xknohub"><b>@Xknohub</b></a> برای گروه فری پروکسی.

</div>