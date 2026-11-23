Как загрузить Pig Monitor 20.0.2 на GitHub
1. Создайте пустой репозиторий на GitHub (например, pig-monitor). Не добавляйте при создании README или LICENSE — они уже находятся в проекте.
2. Распакуйте PigMonitor_GitHub_Repository_v20_0_2.zip.
3. Откройте терминал в распакованной папке и выполните:
git init
git add .
git commit -m "Release Pig Monitor 20.0.2"
git branch -M main
git remote add origin https://github.com/ВАШ_АККАУНТ/pig-monitor.git
git push -u origin main
4. Откройте вкладку Actions. Workflow Pig Monitor CI автоматически запустит Python/Go/Android проверки, соберёт Windows x64/x86 установщики и Android debug APK.
5. Готовые бинарные файлы будут доступны в разделе Artifacts у успешного запуска workflow.
Что попадёт в репозиторий
- исходники сервера, веб-панели, Windows-клиента и Android-приложения;
- выбранные GIF и иконки;
- build scripts и документация;
- GitHub Actions CI workflow.
Папка dist/ и отдельные собранные установщики не добавляются в source repository. Они создаются скриптом или workflow. Файл clientsetup/assets/PigMonitorClient.exe оставлен в исходниках, потому что Go //go:embed использует его как вход для сборки client setup; scripts/build_all_windows.* пересобирает его перед упаковкой.
Лицензия
Открытая лицензия проекта пока не выбрана. GitHub не выдаёт пользователям право повторно использовать код только потому, что репозиторий публичный. Добавьте подходящую лицензию до публикации, если хотите разрешить стороннее использование.
