# Лендинг Selector Casino — тестовое задание

Одностраничный лендинг в стиле сайта Selector: шапка, оффер с промокодом, бонусы, игры, обзор (текст + таблицы + скриншоты), FAQ, подвал.

## Стек
- Семантический HTML5 (`header`, `main`, `section`, `article`, `aside`, `footer`)
- CSS без фреймворков, mobile-first, переменные в `:root`, BEM-именование
- Flexbox для шапки, кнопок, карточек; CSS Grid для сеток игр, бонусов, скриншотов и макета «статья + сайдбар»
- Чистый JS (~4 КБ): бургер-меню, копирование промокода, липкая кнопка на мобильных (IntersectionObserver), лайтбокс на `<dialog>`
- FAQ на нативном `<details>` — без JS

## Производительность
- Шрифт Rubik хранится локально (woff2, только кириллица и латиница), `font-display: swap`, preload
- Картинки в WebP с `width/height` (CLS = 0), `loading="lazy"` для всего, что ниже первого экрана
- Главная иллюстрация — SVG 3 КБ с `fetchpriority="high"`; скрипт с `defer`
- Lighthouse (mobile): Performance 100 · Accessibility 100 · Best Practices 100 · SEO 100

## Структура
```
index.html
css/style.css
js/main.js
img/            иллюстрации, превью игр, скриншоты (webp/svg)
fonts/          Rubik woff2
go/selector/    заглушка партнёрского редиректа
```
