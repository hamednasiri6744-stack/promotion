# سامانه تخفیف و آفر ورانگر — Android RC1

این پروژه، موتور Python نسخه دسکتاپ را مستقیماً داخل APK اجرا می‌کند. پردازش آفلاین است و فایل‌ها از گوشی خارج نمی‌شوند.

## قابلیت‌های نسخه سریع

- انتخاب فایل `اطلاعات کالا.xlsx`
- انتخاب فایل `PROMOTION.xlsx`
- انتخاب فایل `POUYA.xlsx`
- انتخاب پوشه خروجی با Storage Access Framework
- اجرای همان موتور Production Python
- ساخت سه فایل استانی و دوازده شیت
- انتقال Excelها، گزارش JSON و CSV قوانین ردشده به پوشه انتخابی
- رابط فارسی و RTL
- معماری ARM64 مناسب گوشی‌های جدید، از جمله Poco X6 Pro

## ساخت APK با GitHub Actions

1. یک Repository خالی در GitHub بسازید.
2. همه محتویات این پوشه را در ریشه Repository قرار دهید.
3. Push کنید.
4. وارد تب `Actions` شوید.
5. Workflow با نام `Build Android APK` را اجرا کنید.
6. پس از سبزشدن Build، Artifact با نام زیر را دانلود کنید:

```text
VaranegarPromotionEngine-Android-RC1
```

فایل داخل Artifact:

```text
app-debug.apk
```

## ساخت در Android Studio

- Android Studio جدید
- JDK 17
- Android SDK Platform 35
- Android Build Tools 35.0.0
- Gradle 8.10.2

پروژه را باز کنید و از مسیر زیر Build بگیرید:

```text
Build > Build APK(s)
```

## محدودیت RC1

این نسخه فقط ABI `arm64-v8a` را تولید می‌کند. برای اکثر گوشی‌های جدید Android مناسب است. این نسخه هنوز روی دستگاه فیزیکی نصب و تست UI نشده است؛ تست نهایی باید روی گوشی انجام شود.
