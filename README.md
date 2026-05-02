# Клиентский сервис ИИ 3.0 — Презентация

Self-contained интерактивная презентация в стиле Freedom Tech.
Тёмная тема, glassmorphism, WebGL mesh-gradient фон.

## Структура

```
.
├── index.html
├── assets/             ← картинки и SVG
│   ├── freedom-tech.svg     Freedom Tech логотип
│   ├── speaker.png          Ruslan Imirov
│   ├── menu-1/2/3.svg       3 варианта меню
│   ├── cps-agent.svg        CPS chat mockup
│   ├── digest-lock.svg      Digest на lockscreen
│   ├── digest-chat.svg      Digest в чате
│   ├── voice-chat.png       Voice AI экран
│   └── ...
├── README.md
└── .gitignore
```

## 9 слайдов

1. **Cover** — Клиентский сервис ИИ 3.0 + спикер Ruslan Imirov
2. **Analytics** — динамика обращений за 9 месяцев
3. **Customer Journey** — 3 варианта меню + live cust-dev
4. **CPS · Architecture** — Agent-Led Orchestration
5. **Digest Agent** — гипер-персонализация (lockscreen + in-chat)
6. **Voice AI** — голосовой ИИ через WebRTC
7. **MCP** — три контура Model Context Protocol
8. **Portfolio Battle** — игровая механика, лидерборд, призовой фонд
9. **Q&A** — финал

## Управление

- **← → / Space / PageDown** — следующий
- **↑ ↓ / PageUp** — предыдущий
- **Home / End** — первый / последний
- **1-9** — прыжок
- **F** — fullscreen
- **Touch swipe** на мобильных

## Локальный запуск

```bash
python3 -m http.server 8000
```

Откроется на http://localhost:8000

## Деплой на GitHub Pages

```bash
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin git@github.com:<user>/<repo>.git
git push -u origin main
```

Затем **Settings → Pages → Source: main / (root)**.
