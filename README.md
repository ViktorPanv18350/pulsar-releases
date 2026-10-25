# Pulsar

[Українська](#українська) · [English](#english)

## Українська

**Pulsar** — локальна аналітика завантаження команди поверх Redmine або Freshdesk: дашборди, конструктор звітів і
AI-асистент P.U.L.S.E. Дані лежать на вашому компʼютері, спільної бази немає.

Потрібен **Мак на Apple Silicon** (M1 і новіші). Для Windows і Маків на Intel збірок немає.

### Як встановити

1. **Скачайте.** Відкрийте [останній реліз](https://github.com/ViktorPanv18350/pulsar-releases/releases/latest) і в
   розділі «Assets» скачайте `Pulsar-<версія>-arm64.dmg`.
2. **Встановіть.** Відкрийте DMG і перетягніть Pulsar у теку «Програми».
3. **Перший запуск.** Pulsar поки не підписаний сертифікатом Apple, тож macOS скаже, що не може перевірити розробника,
   і не відкриє його. Це очікувано: відкрийте **Системні налаштування → Конфіденційність і безпека**, прокрутіть донизу
   до рядка про Pulsar, натисніть **«Все одно відкрити»** і підтвердьте. Далі Pulsar відкривається як звичайно.
4. **Якщо macOS пише, що Pulsar «пошкоджений» і його треба викинути,** — файл цілий: так macOS позначає все, що
   скачано з інтернету без підпису. Відкрийте «Термінал» і виконайте команду. Вона знімає з Pulsar позначку «скачано з
   інтернету» (карантин) і більше нічого не змінює:

   ```bash
   xattr -dr com.apple.quarantine /Applications/Pulsar.app
   ```

5. **Вхід.** Зареєструйтеся у вікні входу (пошта й пароль або Google). Майстер створить перший проєкт: назва,
   джерела (Redmine, Freshdesk чи обидва), підключення, вибір проєктів, пробний синк за 90 днів і аналіз даних. Або
   **спробуйте демо** — Pulsar покаже все на прикладі даних, нічого не підключаючи.

### Оновлення

Pulsar сам перевіряє нові версії: покаже системне сповіщення і плашку «Оновити» внизу бічної панелі, а в «Про Pulsar»
— що змінилося. Кнопка качає інсталятор у «Завантаження» й відкриває його — перетягніть Pulsar у «Програми» поверх
старого. Дані й налаштування лишаються на місці.

### Дізнаватися про релізи

- Є акаунт GitHub — на цій сторінці **Watch → Custom → Releases**: лист на кожен реліз.
- Без акаунта — RSS: [releases.atom](https://github.com/ViktorPanv18350/pulsar-releases/releases.atom).

### Що знадобиться

- Ключ API Redmine чи Freshdesk для своїх даних (демо працює без нього).
- Для P.U.L.S.E. — ключ Anthropic API або встановлений Claude Code. Інструменти підключень MCP P.U.L.S.E. викликає лише
  з ключем API.

### Щось не так

Меню акаунта → **«Повідомити про баг»**: Pulsar збере опис і діагностику без ваших даних і ключів.

## English

**Pulsar** is local team workload analytics on top of Redmine or Freshdesk: dashboards, a report builder and the
P.U.L.S.E. AI assistant. Your data stays on your computer; there is no shared database.

You need an **Apple Silicon Mac** (M1 or newer). There are no builds for Windows or Intel Macs.

### Install

1. **Download.** Open the [latest release](https://github.com/ViktorPanv18350/pulsar-releases/releases/latest) and
   download `Pulsar-<version>-arm64.dmg` from “Assets”.
2. **Install.** Open the DMG and drag Pulsar into Applications.
3. **First launch.** Pulsar is not signed with an Apple certificate yet, so macOS says it cannot verify the developer
   and will not open it. That is expected: open **System Settings → Privacy & Security**, scroll down to the line about
   Pulsar, click **“Open Anyway”** and confirm. After that Pulsar opens as usual.
4. **If macOS says Pulsar is “damaged” and should be moved to the Bin,** the file is fine: macOS marks everything
   downloaded without a signature this way. Open Terminal and run the command below. It removes the “downloaded from
   the internet” mark (quarantine) from Pulsar and changes nothing else:

   ```bash
   xattr -dr com.apple.quarantine /Applications/Pulsar.app
   ```

5. **Sign in.** Create an account in the sign-in window (email and password, or Google). The wizard creates your first
   project: name, sources (Redmine, Freshdesk or both), connection, project selection, a 90-day trial sync and data
   analysis. Or **try the demo** — Pulsar shows everything on sample data without connecting anything.

### Updates

Pulsar checks for new versions by itself: you get a system notification and an “Update” pill at the bottom of the
sidebar, and “About Pulsar” shows what changed. The button downloads the installer to Downloads and opens it — drag
Pulsar into Applications over the old one. Your data and settings stay in place.

### Release notifications

- With a GitHub account — on this page, **Watch → Custom → Releases**: an email for every release.
- Without an account — RSS: [releases.atom](https://github.com/ViktorPanv18350/pulsar-releases/releases.atom).

### What you need

- A Redmine or Freshdesk API key for your own data (the demo works without one).
- For P.U.L.S.E. — an Anthropic API key or an installed Claude Code. P.U.L.S.E. calls the tools of MCP connections
  only with an API key.

### Something is wrong

Account menu → **“Report a bug”**: Pulsar collects a description and diagnostics without your data or keys.
