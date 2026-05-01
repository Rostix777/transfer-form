# Клиентский сервис ИИ 3.0 — Презентация

Self-contained интерактивная презентация (один HTML-файл) в стиле Freedom Holding Corp.
Тёмная тема, glassmorphism, WebGL mesh-gradient фон, плавные переходы.

## Содержание презентации

1. **Cover** — Клиентский сервис ИИ 3.0
2. **Customer Journey** — обновлённый клиентский путь и меню (3 варианта + live cust-dev)
3. **CPS · Architecture** — Agent-Led Orchestration
4. **CPS · Security** — Security Session, разделение draft / sign
5. **Digest Agent** — гипер-персонализация контента
6. **Voice AI** — голосовой ИИ через WebRTC
7. **MCP** — три контура Model Context Protocol
8. **Portfolio Battle · Mechanics** — игровая механика
9. **Portfolio Battle · Engine** — движок и распределение наград
10. **Q&A** — финальный слайд

## Управление

- **← → / Space / PageDown** — следующий слайд
- **↑ ↓ / PageUp** — предыдущий
- **Home / End** — первый / последний
- **1-9, 0** — прыжок на конкретный слайд
- **F** — fullscreen
- **Click по точкам внизу** — переход на любой слайд
- **Touch swipe** на мобильных

## Локальный запуск

Просто откройте `index.html` в браузере. Можно двойным кликом — работает с протоколом `file://`.
Если нужен локальный сервер для тестов:

```bash
python3 -m http.server 8000
# открыть http://localhost:8000
```

## Деплой на GitHub Pages

1. Создайте репозиторий на GitHub (например `client-service-ai-3-0`).
2. Запушьте файлы:

```bash
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin git@github.com:<your-username>/<repo-name>.git
git push -u origin main
```

3. В GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. Через 1-2 минуты сайт откроется по адресу `https://<your-username>.github.io/<repo-name>/`.

Альтернатива через UI: на странице репозитория **Add file → Upload files**, перетащить `index.html` и `README.md`, **Commit changes**.

## Деплой на другие хосты (одной командой)

- **Netlify**: `npx netlify-cli deploy --prod --dir=.`
- **Vercel**: `npx vercel --prod`
- **Cloudflare Pages**: загрузить через dashboard, root = `/`, build command пустой.
- **Любой статический хостинг**: просто положите `index.html` в корень.

## Куда вставлять прототипы из Figma

В коде размечены placeholder'ы с классом `.figma-prototype` и комментариями `<!-- TODO: ... -->`.
Замените div'ы внутри них на свои изображения:

```html
<!-- было: -->
<div class="figma-prototype flex-1">
  <div class="figma-hint"> ... </div>
</div>

<!-- станет: -->
<div class="figma-prototype flex-1">
  <img src="figma-menu-a.png" alt="Variant A">
</div>
```

Положите PNG/SVG/GIF из Figma рядом с `index.html` и пропишите имена файлов в `src`.

Места для замены:
- **Slide 2** — 3 прототипа меню (`figma-menu-a/b/c.png`)
- **Slide 4** — sequence diagram CPS (`figma-cps-flow.svg`)
- **Slide 8** — маскот игры (`figma-mascot.png`)

## Технические заметки

- Один файл, никаких build-шагов. Чистый HTML/CSS/JS, шрифты с Google Fonts.
- WebGL-шейдер фона воспроизводит эффект `@paper-design/shaders-react MeshGradient`. Если WebGL недоступен — автоматически включается CSS-фоллбек.
- Адаптивно: 16:9 для проектора + работает на мобильных (touch swipe).
- Цвет акцента: `#2db85a` (Freedom green).
- Шрифты: Plus Jakarta Sans (текст) + JetBrains Mono (код, лейблы).
