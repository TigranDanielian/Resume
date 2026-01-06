# Инструкция по деплою на GitHub Pages

## Шаги для развертывания

### 1. Создайте репозиторий на GitHub

1. Перейдите на [GitHub](https://github.com) и создайте новый репозиторий
2. Назовите его, например, `resume` или `cv`

### 2. Инициализируйте Git и загрузите код

```bash
# Инициализируйте git репозиторий
git init

# Добавьте все файлы
git add .

# Сделайте первый коммит
git commit -m "Initial commit: Resume website"

# Добавьте remote репозиторий (замените YOUR_USERNAME и YOUR_REPO на ваши данные)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Переименуйте ветку в main (если нужно)
git branch -M main

# Загрузите код на GitHub
git push -u origin main
```

### 3. Включите GitHub Pages

1. Перейдите в настройки репозитория: `Settings` → `Pages`
2. В разделе **Source** выберите:
   - **Source**: `GitHub Actions`
3. Сохраните изменения

### 4. Проверьте деплой

1. После пуша кода GitHub Actions автоматически запустит workflow
2. Проверьте статус в разделе **Actions** вашего репозитория
3. После успешного деплоя ваш сайт будет доступен по адресу:
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO/
   ```

### 5. Обновление резюме

После изменения `resume.toml`:

```bash
git add resume.toml
git commit -m "Update resume"
git push
```

GitHub Actions автоматически пересоберет и задеплоит обновленную версию.

## Локальная разработка

Для локальной разработки используйте:

```bash
npm install
npm start
```

Сайт будет доступен на `http://localhost:3000`

## Структура проекта

- `resume.toml` - файл с данными резюме (редактируйте его)
- `build.js` - скрипт для генерации статических JSON файлов
- `.github/workflows/deploy.yml` - автоматический деплой на GitHub Pages
- `data/` - сгенерированные JSON файлы (создаются при сборке)

## Примечания

- Файлы в папке `data/` генерируются автоматически при деплое
- Не коммитьте папку `data/` в репозиторий (она в `.gitignore`)
- GitHub Actions автоматически создаст эти файлы при каждом деплое

