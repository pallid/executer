# executer
Веб-сервис для выполнения кода

по мотивам [публикации](https://infostart.ru/public/936455/)

пример запуска:
```bash
set APP_NAME=executer_1
set LOGGING_CONSOLE=true
set LOGGING_LEVEL=DEBUG
set PORT=8085
cd /d "C:\projects\executer\src"
"C:\OneScript.Web\OneScript.WebHost.exe" --urls http://*:%PORT%
```

Для выполнения кода, сервис принимает POST запросы

пример cURL:

```bash
curl -X POST \
  http://localhost:8087 \
  -H 'Content-Type: application/json' \
  -d '{
        "Параметры": {"ПервоеЗначение": 2, "ВтороеЗначение": 3}, 
        "Скрипт": '\''Результат = Параметры["ПервоеЗначение"] + Параметры["ВтороеЗначение"];'\''
      }'

```