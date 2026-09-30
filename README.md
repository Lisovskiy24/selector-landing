# Лендинг Selector Casino — тестовое задание

Одностраничный лендинг: шапка, оффер с промокодом, бонусы, игры, VIP-баннер, обзор (текст + таблицы + скриншоты), FAQ, подвал.

Визуальный стиль, иконки и иллюстрации — из моего UI-кита iGaming-платформы в Figma: токены цветов, типографика (Manrope + Sora), кнопки, бейджи, Hero Banner, Promo Card, Game Card, Step Card, таблицы.

## Стек
- Семантический HTML5 (`header`, `main`, `section`, `article`, `aside`, `footer`)
- CSS без фреймворков, mobile-first, дизайн-токены в `:root`, BEM-именование
- Flexbox — шапка, кнопки, карточки; CSS Grid — сетки бонусов, игр, шагов, скриншотов и макет «статья + сайдбар»
- Чистый JS (~4 КБ): бургер-меню, копирование промокода, липкая панель на мобильных (IntersectionObserver), лайтбокс на `<dialog>`
- FAQ на нативном `<details>`, иконки — inline SVG-спрайт + `<use>`

## Производительность
- Шрифты локально, woff2 с подмножеством символов, `font-display: swap`, preload
- Картинки в WebP с `width/height` (CLS = 0), отдельный кроп баннера для мобильных через `<picture>`, `loading="lazy"` ниже первого экрана
- Lighthouse (mobile): Performance 99 · Accessibility 100 · Best Practices 100 · SEO 100

## Структура
```
index.html
css/style.css
js/main.js
img/            баннеры, превью игр, медали, скриншоты (webp/svg)
fonts/          Manrope, Sora (woff2)
go/selector/    заглушка партнёрского редиректа
```
