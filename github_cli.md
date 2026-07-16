# Работа с Git и GitHub (CLI)

В рамках работы повторялись шаги преподавателя: основы Git и удалённый репозиторий на GitHub.  
Ниже — разбор ошибок и выполненных команд.

---

## 1. Инициализация репозитория и первый push

![Ошибка при первом push и отсутствие коммитов](screenshots/01-initial-push.png)

Попытка отправить изменения:

```bash
git push -u origin master
```

### Возникшие проблемы

* Ошибка: `src refspec master does not match any`
* В репозитории не было коммитов
* Ветка `master` не существовала (используется `main`)
* GitHub не принимал пароль при `git push`

### Выполненные действия

```bash
git add .
git commit -m "initial commit"
git push -u origin main
```

Для аутентификации использован **Personal Access Token**.

### Результат

* Первый коммит загружен на GitHub
* Локальная `main` связана с `origin/main`

---

## 2. Работа с ветками

![Работа с веткой clean_up](screenshots/02-branches.png)

```bash
git branch
git checkout clean_up
git rm readme-after.txt
git rm readme-now.txt
git commit -m "DELETED"
```

Изменения зафиксированы в ветке `clean_up`.

---

## 3. Слияние веток и удаление временной ветки

```bash
git checkout main
git merge clean_up
git branch -d clean_up
git push
```

Слияние прошло в режиме **fast-forward**, `main` обновлена на GitHub.

---

## 4. Получение изменений из удалённого репозитория

![Получение изменений из GitHub с помощью git pull](screenshots/03-pull.png)

```bash
git pull origin main
```

Локальный репозиторий синхронизирован с GitHub.
