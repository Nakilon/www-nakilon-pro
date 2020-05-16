![](https://github.com/nakilon/www-nakilon-pro/workflows/sync_with_gcs/badge.svg)

По пушу в ветку master этого репозитория содержимое сайта www.nakilon.pro синхронизируется с содержимым соответствующей папки.

Если вы согласны, что это удобно, и тоже хотите так делать:

1. читаем в манах GCP о том, как сделать бакет для своего статического сайта, добавляем в ридеры AllUsers
2. делаем Service account без прав и скачиваем его файл-ключ в формате json
3. в свойствах бакета делаем Object admin-ом этот аккаунт по его имейл-идентификатору
4. в репозитории делаем папки с именами в соответствии с именами бакетов
5. в свойствах репозиотрия создаем переменную secrets с содержимым "<имя бакета 1> <base64 json-файла> <имя бакета 2> <base64 json-файла> ..."
6. делаем `.github` с таким же содержимым, как здесь, пушим
