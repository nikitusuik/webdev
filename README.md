# WebDev — Git и GitHub

Лабораторная работа по основам Git и GitHub: консольные команды, ветки, merge/pull/push и то же самое через GitHub Desktop.  
Отчёт со скриншотами и разбором ошибок.

## Структура

| Файл / папка | Что внутри |
| --- | --- |
| `github_cli.md` | Работа в терминале: первый push, ветки, merge, pull |
| `github_desktop.md` | Те же операции через GitHub Desktop |
| `screenshots/` | Скриншоты выполнения |

---

## Цель работы

1. Создать репозиторий, сделать первый коммит и отправить его на GitHub.
2. Поработать с ветками: создать ветку, внести изменения, смержить в `main`.
3. Синхронизировать локальный репозиторий с удалённым (`pull` / `push`).
4. Повторить базовый workflow в GitHub Desktop и сопоставить кнопки GUI с командами Git.

---

## Часть 1 — Git CLI

**Что делалось.** Инициализация / первый push, ветка `clean_up` (удаление лишних файлов), merge в `main`, `git pull`.

**Типичные ошибки и как решены:**

| Проблема | Причина | Решение |
| --- | --- | --- |
| `src refspec master does not match any` | Нет коммитов / ветка называется `main`, а не `master` | `git add` → `git commit` → `git push -u origin main` |
| GitHub не принимает пароль | Пароли отключены для HTTPS | Personal Access Token |

Подробный разбор со скриншотами: [`github_cli.md`](github_cli.md).

---

## Часть 2 — GitHub Desktop

**Что делалось.** Те же шаги через GUI:

| В Desktop | Эквивалент в Git |
| --- | --- |
| Clone repository | `git clone` |
| Changes | `git status` |
| Staging (галочки у файлов) | `git add` |
| Commit to … | `git commit` |
| Push origin | `git push` |
| Fetch / Pull origin | `git pull` |
| Current branch / Merge | `git branch` / `checkout` / `merge` |

Подробности и скриншоты: [`github_desktop.md`](github_desktop.md).

---

## Как открыть отчёт

1. Откройте этот репозиторий на GitHub или локально.
2. Смотрите `github_cli.md` и `github_desktop.md` — картинки лежат в `screenshots/` и подхватываются относительными путями.
