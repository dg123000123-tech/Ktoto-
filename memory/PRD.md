# PRD: Портфолио веб-разработчика ktoto.dev

## Исходная задача
Улучшение готового портфолио (index.html + style.css) по 5 направлениям: мобильные артефакты, анимации, визуал, производительность, UX-фиксы. Убрать оранжевый курсор. Добавить контент.

## Стек
- HTML5, CSS3 (кастомный)
- Tailwind CDN
- GSAP 3.12.5 + ScrollTrigger
- Google Fonts: Syne + DM Sans

## Что реализовано (2 апреля 2026)

### 1. Мобильные артефакты
- `-webkit-tap-highlight-color: transparent` на всех элементах
- `*:focus { outline:none }` + `:focus-visible` для accessibility
- `touch-action: manipulation` на body

### 2. Анимации
- `lazy: false`, `fastScrollEnd: true` во всех ScrollTrigger
- `will-change: transform` только на анимируемых элементах, снимается через `onComplete`
- Параллакс мыши: throttle через requestAnimationFrame flag
- clipPath `inset(100% 0% 0% 0%)` → `none` для карточек (open bottom-up)
- Theme flash: `clip-path: circle()` expanding из точки клика через GSAP
- Split-text hero: каждое слово в `span.word-wrap > span.word-inner` с `translateY(110%) → 0`
- Count-up числа: scale pulse на каждый инкремент

### 3. Визуал
- Карточки: accent-colored box-shadow при hover
- `.btn-primary`: gradient background с `background-position` shift при hover
- Cursor ring: `border-radius → 12px` (rounded rect) при hover на кнопках
- Оранжевый курсор (`.cursor`): `display: none`

### 4. Производительность
- Курсор скрыт на touch: `@media (pointer: coarse)`
- Параллакс отключён на мобильных
- `transform: translateZ(0)` на элементах с backdrop-filter
- `font-display: swap` подтверждён в Google Fonts URL
- Blobs: только `transform: translate()` в keyframes
- `@media (prefers-reduced-motion: reduce)` — отключает все анимации

### 5. UX-фиксы
- Scroll-hint: скрывается после первого скролла (ScrollTrigger `once: true`)
- `avail-badge`: скрыт на `max-width: 520px`
- Магнитные кнопки отключены на touch-устройствах

### 6. Новый контент
- Карточка "Node.js & API"
- Карточка "Lighthouse Performance 98+"
- Stack Marquee секция с технологиями

## Архитектура
- `/app/index.html` — основной файл (canonical)
- `/app/style.css` — стили
- `/app/frontend/public/` — копии для обслуживания через React dev server

## Бэклог
- P1: Добавить секцию с портфолио/кейсами
- P1: SEO meta-теги (og:image, description)
- P2: Lazy loading для изображений (когда добавятся)
- P2: Сохранение выбранной темы в localStorage
