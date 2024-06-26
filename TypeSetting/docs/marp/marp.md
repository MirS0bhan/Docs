
# مارپ چیست و برای چه موردی استفاده می‌شود؟
مارپ یک ابزار قدرتمند برای ایجاد اسلایدها با استفاده از نوشتن مارک‌داون است. با مارپ، شما می‌توانید داستان‌ها، ارائه‌ها، گزارش‌ها و مقالات خود را به صورت زیبا و حرفه‌ای ارائه دهید[1]. به عنوان مثال، این یک اسلاید با مارپ است:
``` marp
---
theme: gaia
class: lead
---

# اسلاید اول
```
این یک مثال از اسلاید مارپ است. می‌توانید متن‌ها، تصاویر و جداول را به راحتی اضافه کنید.

# سینتکس مارپ:
    - سینتکس مارپ بر اساس CommonMark است. برای ایجاد اسلایدها، از خط افقی (---) برای تقسیم صفحات استفاده می‌شود. به عنوان مثال:
```
---
theme: default
---

# اسلاید اول

این یک اسلاید است.
```
- انواع تم‌های مارپ:
    - مارپ سه تم پیش‌فرض دارد: "default"، "gaia" و "uncover". می‌توانید از این تم‌ها استفاده کنید یا تم‌های سفارشی خود را ایجاد کنید. به عنوان مثال:
```
---
theme: uncover
---

# اسلاید اول
```
این یک اسلاید با تم "uncover" است.

- پراپرتی‌های مارپ:
    - مارپ از پراپرتی‌هایی مانند کلاس و lead & invert پشتیبانی می‌کند. با استفاده از کلاس‌ها، می‌توانید سبک‌ها را با CSS سفارشی تنظیم کنید. به عنوان مثال:
```
---
theme: default
class: lead
---

# اسلاید اول

این یک اسلاید با کلاس "lead" است.
```


# نصب Marp CLI و خروجی‌گیری:
برای نصب Marp CLI، می‌توانید از دستورات مربوطه استفاده کنید. سپس با استفاده از این ابزار، می‌توانید اسلایدهای خود را به فرمت‌های HTML، PDF و PowerPoint تبدیل کنید[1].
با استفاده از مارپ، اسلایدهای زیبا و جذاب خود را ایجاد کنید و با دیگران به اشتراک بگذارید! 😊
[1]: https://marp.app/ "مارپ"


به خوبی! حالا به شما توضیح می‌دهم که چگونه از Marp CLI استفاده کنید. Marp CLI یک رابط خط فرمان برای Marp و هر نوع تبدیل‌کننده اسلاید مبتنی بر چارچوب Marpit است. با استفاده از این ابزار، می‌توانید فایل‌های مارک‌داون Marp / Marpit را به HTML / CSS استاتیک، PDF، سند PowerPoint و تصویر (ها) تبدیل کنید1.
در ادامه، دستورات کامند لاین Marp CLI را برای تبدیل اسلایدها به فرمت‌های مختلف توضیح می‌دهم:
- تبدیل اسلایدها به HTML:
    - برای تبدیل یک اسلاید دیکه به فرمت HTML، از دستور زیر استفاده کنید:
``` bash
npx @marp-team/marp-cli@latest slide-deck.md -o output.html
```
- تبدیل اسلایدها به PDF:
    - برای تبدیل یک اسلاید دیکه به فرمت PDF، از دستور زیر استفاده کنید:
``` bash
npx @marp-team/marp-cli@latest slide-deck.md --pdf -o output.pdf
```
- تبدیل اسلایدها به سند PowerPoint (PPTX):
    - برای تبدیل یک اسلاید دیکه به فرمت سند PowerPoint، از دستور زیر استفاده کنید:
``` bash
npx @marp-team/marp-cli@latest slide-deck.md --pptx -o output.pptx
```
- حالت تماشا (Watch mode):
    - با استفاده از حالت تماشا، می‌توانید تغییرات در فایل‌های مارک‌داون را به صورت زنده مشاهده کنید:
``` bash
npx @marp-team/marp-cli@latest -w slide-deck.md
```
- حالت سرور (Server mode):
    - برای استفاده از حالت سرور، باید دایرکتوری مورد نظر را به عنوان پارامتر به دستور اضافه کنید:
``` bash
npx @marp-team/marp-cli@latest -s ./slides
```
در این حالت، فایل تبدیل‌شده به عنوان نتیجه دسترسی به سرور و نه به دیسک خروجی داده می‌شود. شما می‌توانید پورت سرور را با تنظیم متغیر محیطی PORT تعیین کنید. به عنوان مثال، PORT=5000 marp -s ./slides بر روی پورت ۵۰۰۰ گوش می‌دهد1.

 نصب با Docker:
    - اگر نمی‌خواهید Node.js و Chrome را به صورت محلی نصب کنید، می‌توانید از تصویر رسمی Docker marpteam/marp-cli استفاده کنید. برای اطلاعات بیشتر، به Docker Hub مراجعه کنید1.
