# RMTV Landing Page

[العربية](#العربية) | [English](#english)

## العربية

صفحة هبوط عربية باتجاه من اليمين إلى اليسار لخدمة RMTV. تعرّف بالخدمة، وتعرض مجموعات القنوات ومزايا المنتج، وتوجّه الزوار إلى خيارات Android وAndroid TV والويب وiOS وTelegram.

### المزايا

- تخطيط عربي متجاوب لشاشات الحاسوب المكتبي والجهاز اللوحي والهاتف المحمول.
- شريط تنقل ثابت مع تمرير سلس إلى أقسام الصفحة.
- قسم رئيسي يتضمن إجراءات المشاهدة عبر الويب والتنزيل.
- عرض إحصاءات الخدمة وثلاث بطاقات لمجموعات القنوات.
- بطاقات مزايا للسرعة وجودة HD ودعم الأجهزة والواجهة البسيطة.
- تنزيل مباشر لحزمة Android APK المرتبطة حالياً بالصفحة.
- رمز Android TV لتطبيق Downloader مع إجراء للنسخ إلى الحافظة وإشعار تأكيد منبثق.
- روابط خارجية إلى تطبيق RMTV على الويب وقناة Telegram.
- شعارات وصور قنوات وصور منصات وخط مخصص محفوظة محلياً.

### التقنيات المستخدمة

- HTML5
- CSS3 مع استعلامات وسائط للتصميم المتجاوب
- JavaScript خام
- ملف خط AppFont محلي
- Google Fonts (Inter) كخط احتياطي

### التشغيل محلياً

لا حاجة إلى خطوة بناء أو تثبيت حزم.

1. افتح نافذة أوامر في مجلد المشروع.
2. شغّل خادم ملفات ثابتة:

   ```bash
   python -m http.server 8000
   ```

3. افتح `http://localhost:8000` في المتصفح.

يُنصح باستخدام المضيف المحلي لأن الوصول إلى حافظة المتصفح قد لا يعمل عند فتح `index.html` مباشرة كملف. تحتاج الصفحة أيضاً إلى اتصال بالإنترنت لتحميل خط Google والوصول إلى وجهتي الويب وTelegram الخارجيتين.

### بنية المشروع

```text
.
|-- index.html
`-- assets/
    |-- appfont.ttf
    |-- images/              # صور العلامة التجارية والقنوات والمنصات
    `-- apk/
        |-- RM TV V1.3.apk   # الملف المرتبط بزر تنزيل Android
        `-- rmtv_V2.1.apk    # ملف موجود ضمن الحزمة لكنه غير مرتبط بالصفحة
```

### الحالة الحالية

هذه صفحة هبوط ثابتة من دون واجهة خلفية أو نظام بناء أو مدير حزم أو اختبارات آلية. يشير زر تنزيل Android حالياً إلى `RM TV V1.3.apk`؛ ويوجد ملف `rmtv_V2.1.apk` في المستودع، لكن `index.html` لا يشير إليه. رمز Android TV وروابط الوجهات الخارجية مكتوبة مباشرة داخل الصفحة.

لا يتضمن هذا المستودع ملف ترخيص على مستوى المشروع.

## English

An Arabic, right-to-left landing page for RMTV. It introduces the service, presents channel groups and product features, and directs visitors to Android, Android TV, web, iOS, and Telegram options.

### Features

- Responsive Arabic layout for desktop, tablet, and mobile screens.
- Fixed navigation with smooth scrolling to page sections.
- Hero section with web viewing and download actions.
- Displayed service statistics and three channel-group cards.
- Feature cards for speed, HD quality, device support, and a simple interface.
- Direct download of the packaged Android APK currently linked by the page.
- Android TV Downloader code with a clipboard copy action and confirmation toast.
- External links to the RMTV web application and Telegram channel.
- Local logos, channel artwork, platform images, and a custom font.

### Tech Stack

- HTML5
- CSS3 with responsive media queries
- Vanilla JavaScript
- Local AppFont font file
- Google Fonts (Inter) as a fallback

### Run Locally

No build step or package installation is required.

1. Open a terminal in the project directory.
2. Start a static file server:

   ```bash
   python -m http.server 8000
   ```

3. Open `http://localhost:8000` in a browser.

Using localhost is recommended because browser clipboard access may not work when `index.html` is opened directly as a file. The page also needs internet access for the Google font and its external web and Telegram destinations.

### Project Structure

```text
.
|-- index.html
`-- assets/
    |-- appfont.ttf
    |-- images/              # Brand, channel, and platform artwork
    `-- apk/
        |-- RM TV V1.3.apk   # File linked by the Android download button
        `-- rmtv_V2.1.apk    # Packaged file present but not linked by the page
```

### Current Status

This is a static landing page with no backend, build system, package manager, or automated tests. The Android download button currently points to `RM TV V1.3.apk`; the `rmtv_V2.1.apk` file is present in the repository but is not referenced by `index.html`. The Android TV code and external destination links are hard-coded in the page.

No project-level license file is included in this repository.
