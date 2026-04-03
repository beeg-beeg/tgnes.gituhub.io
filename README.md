# 🎮 NES Emulator — Telegram Web App

NES эмулятор на базе [jsnes](https://github.com/bfirsh/jsnes), адаптированный под Telegram Web App.

## 🚀 Деплой на GitHub Pages

### 1. Создай репозиторий

```bash
git init
git add .
git commit -m "init: NES Telegram Web App"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/nes-tg-app.git
git push -u origin main
```

### 2. Включи GitHub Pages

Перейди в репозиторий → **Settings** → **Pages**  
Source: `Deploy from a branch` → Branch: `main` / `/ (root)`  
Нажми **Save**.

Через ~1 минуту сайт будет доступен по адресу:  
`https://YOUR_USERNAME.github.io/nes-tg-app/`

### 3. Подключи к Telegram боту

1. Открой [@BotFather](https://t.me/BotFather) в Telegram
2. Выбери своего бота → **Bot Settings** → **Menu Button**
3. Введи URL: `https://YOUR_USERNAME.github.io/nes-tg-app/`
4. Введи название кнопки, например: `🎮 Play NES`

Или через команду:
```
/setmenubutton
```

### 4. Альтернативно — через inline кнопку

```python
from telegram import InlineKeyboardButton, InlineKeyboardMarkup

keyboard = [[InlineKeyboardButton(
    "🎮 Play NES",
    web_app=WebAppInfo(url="https://YOUR_USERNAME.github.io/nes-tg-app/")
)]]
```

## 🎮 Управление

| Геймпад | Клавиатура |
|---------|-----------|
| D-Pad | ← ↑ ↓ → |
| A | Z |
| B | X |
| START | Enter |
| SELECT | Shift |

## 📁 Где взять ROM-файлы

ROM-файлы `.nes` — это homebrew игры или собственные ROM-ы.  
Примеры легальных homebrew: [nesworld.com](http://www.nesworld.com/article.php?system=nes&data=neshomebrew)

## ⚙️ Возможности

- 📂 Загрузка `.nes` файлов (до 4MB)
- 💾 4 слота сохранения состояния
- 🔊 Звук через Web Audio API
- ⚡ Регулировка скорости: ½× / 1× / 2×
- 📱 Тач-геймпад с поддержкой свайпа
- ⌨️ Клавиатура на десктопе
- 📺 CRT-эффект (scanlines + виньетка)

## 📄 Лицензия

jsnes: Apache-2.0 © Ben Firshman
