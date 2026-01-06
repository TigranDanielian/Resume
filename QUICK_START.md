# 🚀 Быстрый старт для деплоя на GitHub Pages

## 1. Создайте репозиторий на GitHub

1. Зайдите на [github.com](https://github.com)
2. Нажмите "New repository"
3. Назовите репозиторий (например, `resume` или `cv`)
4. **Не** создавайте README, .gitignore или лицензию (всё уже есть)

## 2. Загрузите код

Выполните в терминале в папке проекта:

```bash
# Инициализируйте git (если ещё не сделано)
git init

# Добавьте все файлы
git add .

# Сделайте первый коммит
git commit -m "Initial commit: Resume website"

# Добавьте ваш GitHub репозиторий (замените YOUR_USERNAME и YOUR_REPO)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Переименуйте ветку в main
git branch -M main

# Загрузите код
git push -u origin main
```

## 3. Включите GitHub Pages

1. В репозитории нажмите **Settings** (вверху справа)
2. В левом меню выберите **Pages**
3. В разделе **Source** выберите: **GitHub Actions**
4. Сохраните (если нужно)

## 4. Готово! 🎉

- GitHub Actions автоматически соберёт и задеплоит ваш сайт
- Проверьте статус в разделе **Actions** (вкладка вверху репозитория)
- Через 1-2 минуты ваш сайт будет доступен по адресу:
  ```
  https://YOUR_USERNAME.github.io/YOUR_REPO/
  ```

## Обновление резюме

После изменения `resume.toml`:

```bash
git add resume.toml
git commit -m "Update resume"
git push
```

Сайт автоматически обновится через 1-2 минуты.

---

**Нужна помощь?** Смотрите [DEPLOY.md](./DEPLOY.md) для подробной инструкции.

