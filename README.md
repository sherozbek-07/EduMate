# EduMate — o'qituvchi yordamchisi

O'qituvchi diktant yoki yozma ishni telefonda rasmga oladi. EduMate rasmdagi qo'lyozmani sun'iy intellekt yordamida o'qiydi, asl matn bilan solishtiradi, xatolarni ko'rsatadi va baho qo'yadi. Bitta ishni qo'lda tekshirish taxminan 3 daqiqa oladi, EduMate bilan esa taxminan 30 soniya.

## Imkoniyatlar
- **Diktant**: asl matn bilan solishtirish, imlo va ishora xatolari, to'g'ri yozilishi
- **Yozma mashq**: asl matnsiz, o'zbek tili qoidalari bo'yicha tekshirish va izoh
- Bir yo'la bir nechta rasmni tekshirish (har bir rasm — bitta o'quvchi)
- Bahoni avtomatik qo'yish (me'yorni sozlamalarda o'zgartirish mumkin)
- "Xato emas" tugmasi: AI adashsa, o'qituvchi xatoni o'chiradi
- Jurnal: barcha natijalar, o'rtacha baho, CSV ko'rinishida Excelga ko'chirish
- Tejalgan vaqt statistikasi

## AI kaliti
Ilova ichida: **Sozlamalar → API kalit**.
- Google Gemini (bepul): https://aistudio.google.com/apikey
- yoki Anthropic Claude: https://console.anthropic.com

## APK olish (GitHub Actions)
1. Shu papkani GitHub repozitoriyaga yuklang (`main` branch).
2. GitHub → **Actions** → "APK yig'ish" avtomatik ishga tushadi (~5-7 daqiqa).
3. Tugagach, run sahifasining pastidagi **Artifacts → EduMate-apk** ni yuklab oling, zip ichida `app-debug.apk` bor.
4. APK'ni telefonga o'rnating ("Noma'lum manbalardan o'rnatish"ga ruxsat bering).

## APK olish (Android Studio)
```
npm install
npx cap sync android
npx cap open android
```
Android Studio'da: **Build → Build APK(s)**.

## Kodni o'zgartirish
Butun ilova bitta faylda: `www/index.html`. O'zgartirgandan keyin `npx cap sync android`.
