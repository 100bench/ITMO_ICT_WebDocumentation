# Быстрый старт: Деплой документации на GitHub Pages

## ✅ Что уже готово

- **MkDocs настроен** с Material темой
- **GitHub Actions** для автоматического деплоя
- **Структура документации** готова
- **Локальная сборка** работает

## 🚀 Пошаговый деплой

### 1. Создайте репозиторий на GitHub
- Название: `ITMO_ICT_WebDocumentation`
- Сделайте его публичным

### 2. Загрузите файлы
Скопируйте все файлы из папки `mkdocs_from_user` в корень репозитория:
```
├── .github/workflows/deploy.yml
├── docs/
│   ├── Img/           # ← Добавьте сюда скриншоты
│   ├── index.md
│   └── Lr1.md
├── extra.css
├── mkdocs.yml
├── requirements.txt
└── README.md
```

### 3. Добавьте скриншоты
Поместите в папку `docs/Img/` файлы с именами:
- `part1_server.png`, `part1_client.png`
- `pt2_client.png`, `pt2_server.png`
- `pt3_server.png`, `pt3_console.png`
- `pt4_client1.png`, `pt4_client2.png`, `pt4_client3.png`
- `pt5.1.png`, `pt5.2_exc.png`, `pt5.3_exc.png`
- `image-1.png`

### 4. Настройте GitHub Pages
1. Перейдите в **Settings** → **Pages**
2. В разделе **Source** выберите **GitHub Actions**
3. Сохраните настройки

### 5. Задеплойте
```bash
git add .
git commit -m "Initial commit with MkDocs documentation"
git push origin main
```

### 6. Готово! 🎉
Через 2-3 минуты ваш сайт будет доступен по адресу:
**https://mackb.github.io/ITMO_ICT_WebDocumentation/**

## 🔧 Локальная разработка

```bash
# Установка зависимостей
pip install -r requirements.txt

# Запуск локального сервера
mkdocs serve

# Сайт будет на http://127.0.0.1:8000
```

## 📝 Обновление документации

1. Внесите изменения в `.md` файлы
2. Закоммитьте и запушьте:
   ```bash
   git add .
   git commit -m "Update documentation"
   git push origin main
   ```
3. GitHub Actions автоматически обновит сайт

## ⚠️ Возможные проблемы

- **Скриншоты не отображаются** → проверьте имена файлов в `docs/Img/`
- **Сайт не обновляется** → проверьте статус в разделе **Actions**
- **Ошибки сборки** → проверьте синтаксис markdown

## 📞 Поддержка

Если что-то не работает, проверьте:
1. Все файлы загружены в репозиторий
2. GitHub Pages настроен на GitHub Actions
3. Скриншоты имеют правильные имена
4. Ветка называется `main` или `master`
