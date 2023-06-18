# Chrome DevTools

## Network

Дублирование запроса на сервер `www.1cont.ru` для получения одинакового изображения
![Дублирование](./images/ordinary/network-duplication.png)

Лишний размер ресурса наблюдается у ресурсов `base.js`, `community.js`, `sdk.js`
![Лишний размер](./images/ordinary/network-redundant-size.png)

Долгая загрузка у `auth_check`, `utmEventManager.js`, самого документа
![Долгая загрузка](./images/ordinary/network-long-loading.png)

Много блокирующих ресурсов: `360_light.js`, `code.js`, `tag.js`, `userip`, `context.js`
![Блокирующие](./images/ordinary/network-blocking-requests.png)

## Performance

#### Время событий

- FP: 731.90ms
- FCP: 731.90ms
- LCP: 1.3s
- DCL: 5.33s
- L: 15.53s

#### LCP DOM элемент

Заголовок страницы является LCP элементом

```css
body > div.container-fluid.defaultBackground > div.row.body__wrapper > div.body > div > div.frontpageTop__content.frontpageTop__content_inside.frontpageTop__content_article-item > div.row > div:nth-child(2) > h1
```

#### Время этапов

- Loading: 225ms
- Scripting: 4849ms
- Rendering: 2124ms
- Painting: 119ms

## Coverage

#### Unused CSS: 563kB

#### Unused JS: 2355kB

![Coverage](./images/ordinary/coverage.png)

# Chrome DevTools - 4x Slowdown 3G Throttling

## Network

Дублирование запроса `code.js`, `collect`, `user-recognition`
![Дублирование](./images/throttling/network-duplication-code.png)
![Дублирование](./images/throttling/network-duplication-collect.png)
![Дублирование](./images/throttling/network-duplication-user-recognition.png)

Лишний размер ресурса наблюдается у ресурсов `base.js`, `community.js`, `sdk.js`
![Лишний размер](./images/throttling/network-redundant-size.png)

Долгая загрузка у `base.js`, `community.js`, `sdk.js` и других тяжелых файлов
![Долгая загрузка](./images/throttling/network-long-loading.png)

Блокирующий ресурс это `auth_check` в основном, но также `proxima-nova.ttf`
![Блокирующие](./images/throttling/network-blocking-requests.png)

## Performance

#### Время событий

- FP: 9.45s
- FCP: 9.45s
- LCP: 21.23s
- DCL: 35.66s
- L: 1.1min

#### LCP DOM элемент

Виджет об использовании cookie самый LCP

```css
body > div.CookieNotifyWidget__wrapper > div > div
```

#### Время этапов

- Loading: 511ms
- Scripting: 23787ms
- Rendering: 15881ms
- Painting: 989ms

## Coverage

#### Unused CSS: 541kB

#### Unused JS: 2355kB

![Coverage](./images/throttling/coverage.png)
