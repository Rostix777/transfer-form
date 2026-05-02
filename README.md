# Клиентский сервис ИИ 3.0 — Презентация

Self-contained интерактивная презентация в стиле Freedom Tech.
Тёмная тема, glassmorphism, WebGL mesh-gradient фон, плавные переходы.

## Структура

```
.
├── index.html          ← открыть в браузере
├── assets/             ← все картинки и SVG из Press Pack
│   ├── ai-logo.svg          AI Assistant orb
│   ├── freedom-tech.svg     Freedom Tech логотип
│   ├── speaker.png          Ruslan Imirov
│   ├── menu-1/2/3.svg       3 варианта меню
│   ├── cps-agent.svg        CPS wizard mockup
│   ├── cps-agent-2.svg      CPS dialog mockup
│   ├── digest-lock.svg      Digest на lockscreen
│   ├── digest-chat.svg      Digest в чате
│   ├── voice-chat.png       Voice AI экран
│   ├── portfolio-battle.png TOP 1 корона
│   └── mcp.svg              MCP визуал
├── README.md
└── .gitignore
```

## Содержание презентации (11 слайдов)

1. **Cover** — Клиентский сервис ИИ 3.0 + спикер Ruslan Imirov
2. **Analytics** — динамика обращений за 9 месяцев
3. **Customer Journey** — 3 варианта меню + live cust-dev
4. **CPS · Architecture** — Agent-Led Orchestration
5. **CPS · Security** — Security Session + мокап wizard
6. **Digest Agent** — гипер-персонализация (lockscreen + in-chat)
7. **Voice AI** — голосовой ИИ через WebRTC
8. **MCP** — три контура Model Context Protocol
9. **Portfolio Battle · Mechanics** — игровая механика + маскот
10. **Portfolio Battle · Engine** — движок и распределение наград
11. **Q&A** — финал

## Управление

- **← → / Space / PageDown** — следующий слайд
- **↑ ↓ / PageUp** — предыдущий
- **Home / End** — первый / последний
- **1-9, 0** — прыжок на конкретный слайд (0 = слайд 10)
- **F** — fullscreen
- **Click по точкам внизу** — переход на любой слайд
- **Touch swipe** на мобильных

## Локальный запуск

```bash
python3 -m http.server 8000
# открыть http://localhost:8000
```

⚠️ Открытие двойным кликом (`file://`) тоже работает, но некоторые браузеры
могут заблокировать локальные SVG/PNG из соображений безопасности — поэтому
лучше через локальный сервер.

## Деплой на GitHub Pages

```bash
git init
git add .
git commit -m "init: presentation v1"
git branch -M main
git remote add origin git@github.com:<your-username>/<repo>.git
git push -u origin main
```

Затем в репо: **Settings → Pages → Source: main / (root) → Save**.
Откроется по адресу `https://<username>.github.io/<repo>/`.

Альтернатива: на странице репо **Add file → Upload files**, перетащить весь
проект (включая папку `assets`), **Commit changes**.

## Деплой на другие хосты

- **Netlify**: `npx netlify-cli deploy --prod --dir=.`
- **Vercel**: `npx vercel --prod`
- **Cloudflare Pages**: загрузить через dashboard, root = `/`, build пустой

Любой статический хостинг — просто положить `index.html` + `assets/` в корень.
