# 🤯 ГОЛОВНИЙ ТEҐ

> Простий посібник з елементів HTML `<head>`

[![Учасники](https://img.shields.io/github/contributors/joshbuchea/head.svg?style=for-the-badge)](https://github.com/joshbuchea/HEAD/graphs/contributors)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg?style=for-the-badge)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Підписатися на @joshbuchea у Mastodon](https://img.shields.io/badge/Follow_@joshbuchea-purple?logo=mastodon&logoColor=white&style=for-the-badge)](https://hachyderm.io/@joshbuchea)

## Зміст

- [Рекомендований мінімум](#рекомендований-мінімум)
- [Елементи](#елементи)
- [Мета-теги](#мета-теги)
- [Посилання](#посилання)
- [Іконки](#іконки)
- [Соціальні мережі](#соціальні-мережі)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter Card](#twitter-card)
  - [Twitter Конфіденційність](#конфіденційність-twitter)
  - [Schema.org](#schemaorg)
  - [Pinterest](#pinterest)
  - [Facebook Миттєві статті](#facebook-instant-articles)
  - [OEmbed](#oembed)
  - [QQ/Wechat](#qqwechat)
- [Браузери / Платформи](#браузери--платформи)
  - [Apple iOS](#apple-ios)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Браузери (Китайські)](#браузери-китайські)
  - [360 Браузер](#360-браузер)
  - [QQ Мобільний Браузер](#qq-мобільний-браузер)
  - [UC Мобільний Браузер](#uc-мобільний-браузер)
- [Посилання на додатки](#посилання-на-додатки)
- [Інші ресурси](#інші-ресурси)
- [Пов'язані проекти](#повязані-проекти)
- [Інші формати](#інші-формати)
- [Переклади](#-переклади)
- [Внесок](#-внесок)
  - [Учасники](#-учасники)
- [Автори](#-автори)
- [Ліцензія](#-ліцензія)

## Рекомендований мінімум

Нижче наведені основні елементи для будь-якого веб-документа (веб-сайти/додатки):

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  Два мета-теги вище ПОВИННІ йти першими в розділі <head>
  щоб послідовно забезпечити правильне відтворення документа.
  Будь-які інші елементи head повинні йти ПІСЛЯ цих тегів.
 -->
<title>Назва сторінки</title>
```

`meta charset` - визначає кодування веб-сайту, `utf-8` є стандартом

`meta name="viewport"` - налаштування viewport, пов'язані з мобільною адаптивністю

`width=device-width` - використання фізичної ширини пристрою (чудово для мобільних!)

`initial-scale=1` - початковий масштаб, 1 означає без масштабування

**[⬆ назад до змісту](#зміст)**

## Елементи

Дійсні елементи `<head>` включають `meta`, `link`, `title`, `style`, `script`, `noscript` та `base`.

Ці елементи надають інформацію про те, як документ повинен сприйматися та відтворюватися веб-технологіями, наприклад, браузерами, пошуковими системами, ботами тощо.

```html
<!--
  Встановіть кодування символів для цього документа, 
  щоб усі символи в просторі UTF-8 (як-от емодзі)
  відображалися правильно.
-->
<meta charset="utf-8">

<!-- Встановіть назву документа -->
<title>Назва сторінки</title>

<!-- Встановіть базову URL-адресу для всіх відносних URL-адрес у документі -->
<base href="https://example.com/page.html">

<!-- Посилання на зовнішній CSS-файл -->
<link rel="stylesheet" href="styles.css">

<!-- Використовується для додавання CSS безпосередньо в документ -->
<style>
  /* ... */
</style>

<!-- Теги JavaScript та No-JavaScript -->
<script src="script.js"></script>
<script>
  // функція(ї) розміщується тут
</script>
<noscript>
  <!-- Альтернатива без JavaScript -->
</noscript>
```

## Мета-теги

```html
<!--
  Наступні 2 мета-теги ПОВИННІ йти першими в розділі <head>
  щоб послідовно забезпечити правильне відтворення документа.
  Будь-які інші елементи head повинні йти ПІСЛЯ цих тегів.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  Дозволяє контролювати звідки завантажуються ресурси.
  Розмістіть якомога раніше в розділі <head>, оскільки тег
  застосовується лише до ресурсів, оголошених після нього.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Назва веб-додатку (використовується лише якщо веб-сайт використовується як додаток) -->
<meta name="application-name" content="Назва Додатку">

<!-- Колір теми для Chrome, Firefox OS та Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Короткий опис документа (обмеження до 150 символів) -->
<!-- Цей вміст МОЖЕ бути використаний як частина результатів пошуку. -->
<meta name="description" content="Опис сторінки">

<!-- Контроль поведінки пошукових павуків при індексації -->
<meta name="robots" content="index,follow"><!-- Всі пошукові системи -->
<meta name="googlebot" content="index,follow"><!-- Специфічно для Google -->

<!-- Вказує Google не показувати поле пошуку сайтлінків -->
<meta name="google" content="nositelinkssearchbox">

<!-- Вказує Google не надавати переклад для цього документа -->
<meta name="google" content="notranslate">

<!-- Перевірка власності веб-сайту -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Яндекс Вебмайстер -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Консоль Alexa -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Консоль Pinterest -->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Визначення програмного забезпечення, використаного для створення документа (наприклад, WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Короткий опис теми вашого документа -->
<meta name="subject" content="тема вашого документа">

<!-- Надає загальну вікову категорію на основі вмісту документа -->
<meta name="rating" content="General">

<!-- Дозволяє контролювати передачу інформації про реферера -->
<meta name="referrer" content="no-referrer">

<!-- Вимкнення автоматичного виявлення та форматування можливих номерів телефонів -->
<meta name="format-detection" content="telephone=no">

<!-- Повністю відмовитися від префетчингу DNS, встановивши значення "off" -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Вказує документ для відображення у певному фреймі -->
<meta http-equiv="Window-Target" content="_value">

<!-- Гео-теги -->
<meta name="ICBM" content="широта, довгота">
<meta name="geo.position" content="широта;довгота">
<meta name="geo.region" content="країна[-область]"><!-- Код країни (ISO 3166-1): обов'язковий, код області (ISO 3166-2): необов'язковий; наприклад, content="UA" / content="UA-KY" -->
<meta name="geo.placename" content="місто"><!-- наприклад, content="Київ" -->

<!-- Монетизація Веб (Web Monetization) https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [Мета-теги, які розуміє Google](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: Розширення мета-тегів](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM у Вікіпедії](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Геотегування у Вікіпедії](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ назад до змісту](#зміст)**

## Посилання

```html
<!-- Посилання на зовнішню таблицю стилів -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Допомагає запобігти проблемам з дубльованим контентом -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- Посилання на AMP HTML-версію поточного документа -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Посилання на JSON-файл, що вказує облікові дані "інсталяції" для веб-додатків -->
<link rel="manifest" href="manifest.json">

<!-- Посилання на інформацію про автора(ів) документа -->
<link rel="author" href="humans.txt">

<!-- Посилається на заяву про авторські права, що застосовується до контексту посилання -->
<link rel="license" href="copyright.html">

<!-- Надає посилання на місце в документі, яке може бути іншою мовою -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Надає інформацію про автора чи іншу особу -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Посилання на документ, що описує збірку записів, документів чи інших матеріалів історичного інтересу -->
<link rel="archives" href="https://example.com/archives/">

<!-- Посилання на ресурс верхнього рівня в ієрархічній структурі -->
<link rel="index" href="https://example.com/article/">

<!-- Надає самопосилання - корисно, коли документ має кілька можливих посилань -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- Перший, останній, попередній і наступний документи в серії документів, відповідно -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Використовується, коли використовується стороння служба для ведення блогу -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Формує автоматичний коментар, коли інший блог WordPress посилається на ваш блог або пост -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Сповіщає URL, коли ви посилаєтеся на нього у вашому документі -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Дозволяє публікувати на власному домені за допомогою клієнта Micropub -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Відкритий пошук -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Назва пошуку">

<!-- Стрічки -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Префетчинг, попереднє завантаження, попереднє перегортання -->
<!-- Більше інформації: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Зв'язки посилань](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ назад до змісту](#зміст)**

## Іконки

```html
<!-- Для IE 10 та нижче -->
<!-- Розмістіть favicon.ico в кореневому каталозі - додатковий тег не потрібен -->

<!-- Іконка в найвищій роздільній здатності, яка нам потрібна -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (повторне використання іконки 192px) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Іконка закріпленої вкладки Safari -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [Все про Favicon (і сенсорні іконки)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Створення іконок закріплених вкладок](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Шпаргалка з Favicon](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Іконки та кольори браузера](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ назад до змісту](#зміст)**

## Соціальні мережі

### Facebook Open Graph
> Більшість контенту діляться на Facebook як URL, тому важливо позначити ваш веб-сайт тегами Open Graph, щоб мати контроль над тим, як виглядає ваш контент на Facebook. [Детальніше про розмітку Facebook Open Graph](https://developers.facebook.com/docs/sharing/webmasters#markup)

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Назва Контенту">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="Опис того, що зображено на зображенні (не підпис)">
<meta property="og:description" content="Опис тут">
<meta property="og:site_name" content="Назва Сайту">
<meta property="og:locale" content="uk_UA">
<meta property="article:author" content="">
```

- 📖 [Протокол Open Graph](http://ogp.me/)
- 🛠 Перевірте свою сторінку за допомогою [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card
> За допомогою Twitter Cards ви можете додавати до твітів багаті фото, відео та медіа-контент, допомагаючи збільшити трафік на ваш веб-сайт. [Детальніше про Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@обліковий_запис_сайту">
<meta name="twitter:creator" content="@індивідуальний_обліковий_запис">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Назва Контенту">
<meta name="twitter:description" content="Опис контенту менше 200 символів">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="Текстовий опис зображення, що передає його основну суть для користувачів з вадами зору. Максимум 420 символів.">
```

- 📖 [Початок роботи з картками — Twitter Розробникам](https://dev.twitter.com/cards/getting-started)
- 🛠 Перевірте свою сторінку за допомогою [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Конфіденційність Twitter
Якщо ви вбудовуєте твіти на свій веб-сайт, Twitter може використовувати інформацію з вашого сайту для налаштування контенту та пропозицій для користувачів Twitter. [Детальніше про параметри конфіденційності Twitter](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- заборонити Twitter використовувати інформацію вашого сайту для персоналізації -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Назва Контенту">
      <meta itemprop="description" content="Опис контенту менше 200 символів">
      <meta itemprop="image" content="https://example.com/image.jpg">
```

**Примітка:** Ці мета-теги вимагають додавання атрибутів `itemscope` та `itemtype` до тегу `<html>`.

- 📖 [Початок роботи - schema.org](https://schema.org/docs/gs.html)
- 🛠 Перевірте свою сторінку за допомогою [Rich Results Test](https://search.google.com/test/rich-results)

### Pinterest

Pinterest дозволяє запобігти збереженню вмісту з вашого веб-сайту, відповідно до [їхнього центру допомоги](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). `description` є необов'язковим.

```html
<meta name="pinterest" content="nopin" description="Вибачте, ви не можете зберігати вміст з мого веб-сайту!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- URL веб-версії вашої статті -->
<link rel="canonical" href="https://example.com/article.html">

<!-- Стиль, який буде використано для цієї статті -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Створення статей - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Приклади коду - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="Профіль oEmbed: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="Профіль oEmbed: XML">
```

- 📖 [Формат oEmbed](https://oembed.com/)

### QQ/Wechat

Користувачі діляться веб-сторінками в qq wechat з форматованим повідомленням

```html
<meta itemprop="name" content="назва для спільного використання">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="вміст для спільного використання">
```
- 📖 [Документація з формату коду](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ назад до змісту](#зміст)**

## Браузери / Платформи

### Apple iOS

```html
<!-- Розумний App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Вимкнення автоматичного виявлення та форматування можливих номерів телефонів -->
<meta name="format-detection" content="telephone=no">

<!-- Іконка запуску (180x180px або більше) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Зображення екрану запуску -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Назва іконки запуску -->
<meta name="apple-mobile-web-app-title" content="Назва Додатку">

<!-- Увімкнення автономного (повноекранного) режиму -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Вигляд панелі статусу (не має ефекту, якщо не увімкнено автономний режим) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- Deep linking для iOS додатків -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Налаштування веб-додатків](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Додати на головний екран -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Більше інформації: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Deep linking для Android додатків -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Вимкнення запиту на переклад -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Примусити IE 8/9/10 використовувати найновішу версію рушія рендерингу -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Вимкнення автоматичного виявлення та форматування можливих номерів телефонів розширенням браузера Skype Toolbar -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Плитки Windows -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Мінімально необхідна XML розмітка для `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Довідка зі схеми конфігурації браузера](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

## Браузери (Китайські)

### 360 Браузер

```html
<!-- Вибір порядку рушіїв рендерингу -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

I'll translate the document to Ukrainian:

### QQ Мобільний Браузер

```html
<!-- Блокує екран у вказаній орієнтації -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Показати цей документ у повноекранному режимі -->
<meta name="x5-fullscreen" content="true">

<!-- Документ буде відображатися в "режимі додатку" (повноекранний тощо) -->
<meta name="x5-page-mode" content="app">
```

### UC Мобільний Браузер

```html
<!-- Блокує екран у вказаній орієнтації -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Показати цей документ у повноекранному режимі -->
<meta name="full-screen" content="yes">

<!-- UC браузер буде показувати зображення навіть в "текстовому режимі" -->
<meta name="imagemode" content="force">

<!-- Документ буде відображатися в "режимі додатку" (повноекранний, забороняючи жести тощо) -->
<meta name="browsermode" content="application">

<!-- Вимкнено "нічний режим" UC браузера для цього документа -->
<meta name="nightmode" content="disable">

<!-- Спростити документ для зменшення передачі даних -->
<meta name="layoutmode" content="fitscreen">

<!-- Вимкнути функцію UC браузера "масштабування шрифту, коли в документі багато тексту" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [Документація UC Browser](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ назад до змісту](#зміст)**

## Посилання на додатки

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Резервний веб-варіант -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [Посилання на додатки](https://developers.facebook.com/docs/applinks)

**[⬆ назад до змісту](#зміст)**

## Інші ресурси

- 📖 [Документація HTML5 Boilerplate: HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [Документація HTML5 Boilerplate: Розширення та налаштування](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ назад до змісту](#зміст)**

## Пов'язані проекти

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Пакет Atom для фрагментів `HEAD`
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Пакет Sublime Text для фрагментів `HEAD`
- [head-it](https://github.com/hemanth/head-it) - CLI-інтерфейс для фрагментів `HEAD`
- [vue-head](https://github.com/ktquez/vue-head) - Маніпуляція метаінформацією тегу `HEAD` для Vue.js

**[⬆ назад до змісту](#зміст)**

## Інші формати

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ назад до змісту](#зміст)**

## 🌐 Переклади

- 🇮🇩 [Індонезійська](https://github.com/rijdz/HEAD)
- 🇧🇷 [Бразильська portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Китайська (спрощена)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [Німецька](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Італійська](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Японська](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Корейська](https://github.com/Lutece/HEAD)
- 🇷🇺 [Російська](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Іспанська](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Турецька](https://github.com/mkg0/HEAD)
- 🇺🇦 [Українська](https://github.com/Shramkoweb/HEAD)

**[⬆ назад до змісту](#зміст)**

## 🤝 Внесок

**Відкрийте issue або pull request для пропозиції змін або доповнень.**

### Посібник

Репозиторій **HEAD** складається з двох гілок:

#### 1. `master`

Ця гілка складається з файлу `README.md`, який відображається на веб-сайті [htmlhead.dev](https://htmlhead.dev/). Усі зміни до вмісту посібника мають бути зроблені в цьому файлі.

Дотримуйтесь цих кроків для pull requests:

{:.list-style-default}
- Змінюйте лише один тег або один пов'язаний набір тегів за раз
- Використовуйте подвійні лапки для атрибутів
- Не включайте кінцевий слеш у самозакриваючих елементах — специфікація HTML5 каже, що вони необов'язкові
- Розгляньте можливість включення посилання на документацію, яка підтримує вашу зміну

#### 2. `gh-pages`

Ця гілка відповідає за веб-сайт [htmlhead.dev](https://htmlhead.dev/). Ми використовуємо [Jekyll](https://jekyllrb.com/) для розгортання файлу `README.md` markdown на [GitHub Pages](https://pages.github.com/). Усі модифікації, пов'язані з веб-сайтом, мають бути зроблені в цій гілці.

Вам може бути корисно переглянути [Документацію Jekyll](https://jekyllrb.com/docs/home/) та зрозуміти, як працює Jekyll, перш ніж працювати в цій гілці.

## 🌟 Учасники

Перевірте всіх неймовірних [учасників](https://github.com/joshbuchea/HEAD/graphs/contributors) 🤩

## 👤 Автори

**Джош Бучеа**

- GitHub: [@joshbuchea](https://github.com/joshbuchea)
- Mastodon: [@joshbuchea@hachyderm.io](https://hachyderm.io/@joshbuchea)

**Serhii Shramko**
- GitHub: [@Shramkoweb](https://github.com/Shramkoweb)


## 💛 Підтримка

Якщо цей проект був корисним для вас або вашої організації, будь ласка, розгляньте можливість підтримки моєї роботи безпосередньо:

- 💛 [Спонсоруйте мене на GitHub](https://github.com/sponsors/joshbuchea)
- ⭐️ [Поставте зірочку цьому проекту на GitHub](https://github.com/joshbuchea/HEAD)
- 🐙 [Підписатися на мене на GitHub](https://github.com/joshbuchea)
- 🐘 [Підписатися на мене в Mastodon](https://hachyderm.io/@joshbuchea)

Дякую! 🙏

- [Джош](https://joshbuchea.com/)
- [Serhii Shramko](https://shramko.dev/)

## 📝 Ліцензія

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ назад до змісту](#зміст)**
