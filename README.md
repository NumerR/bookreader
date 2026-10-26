# Читалка — Android APK

## Способ 1. Без Android Studio (через GitHub)
1. Создайте на github.com новый репозиторий (можно приватный).
2. Загрузите в него все файлы из этой папки (Add file → Upload files; папку .github тоже).
3. Вкладка Actions → Build APK → Run workflow. Через 3–5 минут появится артефакт reader-apk.
4. Скачайте архив, распакуйте, перенесите app-debug.apk на телефон и откройте его.
   (Android попросит разрешить установку из неизвестных источников.)

## Способ 2. Локально (нужны Node.js 18+, JDK 17, Android Studio)
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk
