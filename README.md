# Masareef | مصاريف — iOS Capacitor Project

مشروع جاهز لبناء تطبيق **مصاريف (Masareef)** بصيغة `.ipa` غير موقعة (Unsigned IPA) عبر **Codemagic** أو **GitHub Actions** دون الحاجة لحساب مطور Apple مدفوع أو رفعه إلى App Store، بحيث يعمل 100% أوفلاين على الآيفون.

## محتويات المشروع
- `www/index.html`: واجهة التطبيق الكاملة (تعمل بدون إنترنت بالكامل مع حفظ البيانات محلياً).
- `package.json`: إعدادات وحزم Capacitor iOS.
- `capacitor.config.json`: إعدادات التطبيق (`com.alhawari.masareef`).
- `codemagic.yaml`: ملف البناء التلقائي عبر Codemagic لإنتاج `Masareef-unsigned.ipa`.
- `.github/workflows/build-ipa.yml`: ملف البناء التلقائي عبر GitHub Actions لإنتاج `Masareef-unsigned.ipa`.

## البناء عبر Codemagic
1. ارفع جميع ملفات هذا المشروع إلى مستودعك في GitHub (بما في ذلك `codemagic.yaml` و`.github/workflows/build-ipa.yml`).
2. افتح لوحة تحكم **Codemagic** وسجّل الدخول عبر GitHub.
3. اختر المستودع واضغط **Start new build** ثم اختر سير العمل **Masareef Unsigned iOS IPA**.
4. بعد انتهاء البناء، حمّل ملف `Masareef-unsigned.ipa` من قسم **Artifacts** وثبّته على الآيفون عبر Sideloadly أو AltStore أو TrollStore.
