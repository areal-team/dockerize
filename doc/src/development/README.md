# Развертывание проекта для разработчика

## Общая информация
- Репозиторий: https://git.arealidea.ru/arealidea/dockerize
- [Issues](https://git.arealidea.ru/arealidea/dockerize/issues)
- Для удобства разработки в проект добавлена поддержка docker.
- При этом на продуктовом сервере докер может не использоваться.
- Почту можно проверять по [адресу](http://localhost:8025)
- Документация доступна по [адресу](http://localhost/ddoc/)
- [Code style](./code-style.html)


## Начало работы с проектом
- Склонируйте из репозитория:
    ```bash
    git clone ssh://git@git.arealidea.ru:23450/arealidea/dockerize.git
    ```
- Иницализация 
    ```bash
    make init
    ```
- Измените подключение к БД в файле `src/app/bitrix/.settings.php`. Правильные значения прописаны в файле `.env`. Обычно это:
    ```php
    'host' => 'mysql',
    'database' => 'db',
    'login' => 'bitrix',
    'password' => '123',
    ```
- Запуск контейнеров 
    ```bash
    make up
    ```
- Восстановление БД
    ```bash
    make restore-mysql
    ```
- Прочитайте [документацию по проекту](http://localhost/ddoc/)
- Проект доступен по адресу [http://localhost/](http://localhost/)
