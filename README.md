# DeepSite WebView (Android)

Готовый Android-проект на Kotlin c WebView. Загружает локальный `assets/index.html` (офлайн) или может открывать удалённый URL.

## Сборка
1. Откройте папку в Android Studio (Giraffe+).
2. Дождитесь синхронизации Gradle (Android Studio подтянет версии из `settings.gradle`).
3. Запустите на устройстве (Run) или соберите APK: **Build > Build APK(s)**.

## Настройка загрузки контента
По умолчанию загружается `file:///android_asset/index.html`.
Чтобы использовать хостинг, измените строку в `MainActivity.kt`:

```kotlin
// webView.loadUrl("file:///android_asset/index.html")
webView.loadUrl("https://your-public-url")
```

## File upload
Реализован `onShowFileChooser` через SAF (`ACTION_OPEN_DOCUMENT`), системные разрешения на чтение не требуются.

## Пакет
`com.deepsite.webview` — измените при необходимости в манифесте и Gradle.
