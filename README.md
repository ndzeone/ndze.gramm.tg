# ndze.gramm.tg

Открытый форк Telegram со своими функциями. Основан на [Telegram Web A](https://github.com/Ajaxy/telegram-tt)
(лицензия GPL-3.0 — форк тоже открытый). Оригинальный README: [README.upstream.md](README.upstream.md).

Форк сделан с upstream-коммита `090e38f1dffec3e0a9aefbec8159a9931fbeec8f`.

## Как запустить и войти в свой аккаунт (бесплатно)

1. **Получи свои API-ключи** (бесплатно, один раз):
   - зайди на <https://my.telegram.org> → войди по номеру телефона;
   - открой **API development tools** → заполни форму (App title: `ndze.gramm.tg`, Short name: `ndzegramm`, Platform: Web);
   - скопируй `api_id` и `api_hash`.
2. **Создай `.env`:**
   ```sh
   cp .env.example .env
   ```
   и впиши туда `TELEGRAM_API_ID=...` и `TELEGRAM_API_HASH=...`. Файл `.env` не попадает в git.
3. **Установи зависимости и запусти** (нужен Node.js 24.15+):
   ```sh
   npm i
   npm run dev
   ```
4. Открой <http://localhost:1234> → войди по QR-коду из приложения Telegram на телефоне
   (Настройки → Устройства → Подключить устройство) или по номеру телефона.

## Установщики

- **macOS / Windows / Linux** — десктоп-приложение на Tauri (`npm run tauri:build`, нужен Rust),
  сборка через GitHub Actions: workflow «Package and publish» (запуск вручную).
- **Телефон** — веб-версия ставится как приложение (PWA): «Поделиться → На экран „Домой“».
