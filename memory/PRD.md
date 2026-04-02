# PRD: Портфолио веб-разработчика ktoto.dev

## Исходная задача
Улучшение готового портфолио (index.html + style.css). Многоитерационная работа.

## Стек
HTML5, CSS3, Tailwind CDN, GSAP 3.12.5 + ScrollTrigger, Google Fonts (Syne + DM Sans)

## Итерация 1 (2 апреля 2026)
- Мобильные артефакты: tap-highlight, focus-visible, touch-action
- GSAP оптимизация: lazy, fastScrollEnd, will-change cleanup, rAF-throttled parallax
- Визуал: split-text hero, clipPath reveal, clip-path circle() theme flash, gradient button, cursor ring→rounded-rect
- Производительность: prefers-reduced-motion, cursor hidden on touch, parallax off mobile, GPU layers
- UX: scroll-hint auto-hide, avail-badge hidden on small screens
- Убран оранжевый курсор, добавлены 2 карточки + Stack Marquee

## Итерация 2 (2 апреля 2026)
- **Фикс skill-tags**: убрана position:absolute, тэги в нормальном потоке, удалён Tailwind тэг
- **SVG иконки**: все 10 карточек — inline SVG вместо emoji (rocket, zap, code, atom, settings, layout, wind, server)
- **Интерактивные тэги**: клик на HTML/CSS/GSAP меняет иконку карточки "Лендинги" с анимацией (GSAP scale+rotation swap)
- **Секция портфолио**: 4 работы с изображениями (Unsplash), hover-эффекты, тэги технологий
- **Стат скорости**: изменено на "от 1 часа"

## Архитектура
- `/app/index.html` — canonical
- `/app/style.css` — стили
- `/app/frontend/public/` — копии для dev-сервера

## Бэклог
- P1: Реальные проекты в портфолио (свои скриншоты/ссылки)
- P1: SEO meta-теги (og:image, description)
- P2: localStorage сохранение темы
- P2: Модальное окно с деталями проекта при клике на работу
- P3: Форма обратной связи
