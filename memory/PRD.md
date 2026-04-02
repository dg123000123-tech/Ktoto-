# PRD: Портфолио веб-разработчика ktoto.dev

## Стек
HTML5, CSS3, Tailwind CDN, GSAP 3.12.5 + ScrollTrigger, Google Fonts (Syne + DM Sans)

## Итерация 3 (2 апреля 2026)
- **Фикс**: "Посмотреть работы" теперь прокручивает к секции `#works` (портфолио), а не к `#services`
- **Фикс**: страница всегда стартует с самого верха (`history.scrollRestoration = 'manual'` + `scrollTo(0,0)`)
- **Фикс**: фото портфолио заменены на скриншоты реальных сайтов/интерфейсов (Webflow, дашборд, SaaS)

## Реализовано за все итерации
1. Мобильные артефакты, tap-highlight, focus-visible, touch-action
2. GSAP оптимизация (lazy, fastScrollEnd, will-change, rAF-parallax, clipPath reveal, clip-path theme flash)
3. Split-text hero, SVG иконки (вместо emoji), интерактивные тэги на Landing карточке
4. Секция портфолио с 4 работами, Stack Marquee
5. Производительность (prefers-reduced-motion, cursor hidden on touch, GPU layers)

## Бэклог
- P1: Реальные проекты с ссылками
- P2: localStorage тема
- P2: Модальное окно деталей проекта
- P3: Форма обратной связи
