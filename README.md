# Публикация отчета через MkDocs

Шаги
1. Создай пустой репозиторий на GitHub USER REPO
2. Скопируй файлы из этого архива в корень репозитория
3. В mkdocs.yml замени USER и REPO на свои значения
4. Закоммить в ветку main и запушь
5. В настройках репозитория Settings Pages выбери Source GitHub Actions
6. После успешного запуска workflow сайт будет доступен по ссылке вида https://USER.github.io/REPO

Структура
- mkdocs.yml конфигурация сайта
- extra.css пользовательские стили
- docs index.md главная
- docs Lr1.md твой отчет
- docs Img сюда положи скриншоты с теми же именами
- .github workflows deploy.yml публикация на GitHub Pages