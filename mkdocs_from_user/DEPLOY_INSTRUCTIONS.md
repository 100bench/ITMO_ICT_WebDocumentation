# Инструкция по деплою документации на GitHub Pages

## Что уже настроено

✅ **MkDocs конфигурация** - файл `mkdocs.yml` настроен с Material темой  
✅ **GitHub Actions workflow** - автоматический деплой при пуше в main/master  
✅ **Зависимости** - файл `requirements.txt` с необходимыми пакетами  
✅ **Структура документации** - готовые markdown файлы с отчетом  

## Пошаговая инструкция

### 1. Подготовка репозитория

1. Создайте новый репозиторий на GitHub с именем `ITMO_ICT_WebDocumentation`
2. Скопируйте все файлы из папки `mkdocs_from_user` в корень репозитория
3. Добавьте скриншоты в папку `docs/Img/` с именами:
   - part1_server.png, part1_client.png
   - pt2_client.png, pt2_server.png  
   - pt3_server.png, pt3_console.png
   - pt4_client1.png, pt4_client2.png, pt4_client3.png
   - pt5.1.png, pt5.2_exc.png, pt5.3_exc.png
   - image-1.png

### 2. Настройка GitHub Pages

1. Перейдите в Settings → Pages вашего репозитория
2. В разделе "Source" выберите "GitHub Actions"
3. Сохраните настройки

### 3. Деплой

1. Закоммитьте и запушьте все файлы в ветку `main`:
   ```bash
   git add .
   git commit -m "Initial commit with MkDocs documentation"
   git push origin main
   ```

2. GitHub Actions автоматически соберет и задеплоит сайт
3. Через несколько минут сайт будет доступен по адресу:
   `https://mackb.github.io/ITMO_ICT_WebDocumentation/`

### 4. Локальная разработка

Для локального просмотра документации:

```bash
# Установка зависимостей
pip install -r requirements.txt

# Запуск локального сервера
mkdocs serve

# Сайт будет доступен на http://127.0.0.1:8000
```

### 5. Обновление документации

Для обновления документации:
1. Внесите изменения в markdown файлы
2. Закоммитьте и запушьте изменения
3. GitHub Actions автоматически обновит сайт

## Структура файлов

```
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions для деплоя
├── docs/
│   ├── Img/                    # Папка для скриншотов
│   ├── index.md               # Главная страница
│   └── Lr1.md                 # Отчет по лабораторной работе
├── extra.css                  # Пользовательские стили
├── mkdocs.yml                 # Конфигурация MkDocs
├── requirements.txt           # Python зависимости
└── README.md                  # Описание проекта
```

## Возможные проблемы

1. **Скриншоты не отображаются** - проверьте, что файлы находятся в `docs/Img/` с правильными именами
2. **Сайт не обновляется** - проверьте статус GitHub Actions в разделе Actions
3. **Ошибки сборки** - проверьте синтаксис markdown файлов

## Полезные команды

```bash
# Проверка конфигурации
mkdocs build

# Создание статического сайта
mkdocs build --clean

# Просмотр справки
mkdocs --help
```

