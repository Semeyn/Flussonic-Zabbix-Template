# Мониторинг сервера Flussonic в Zabbix
## Описание
Мониторинг Flussonic через встроенное API 
### Шаблон позвояет:
### 1. Мониторить основные показатели сервера:
* Версия
* Время работы
* Загрузка планировщика
* Загрузка процессора
* Количество клиентов
* Количество потоков
* Количество процессов Flussonic
* Ошибки в лог файле
* Количество ошибок в лог файле
* Скорость входящая
* Скорость исходящая
### 2. Мониторить потоки:
* Статус потока
* Ошибки потока
* Ошибки кодирвоания потока
* Количество клиентов
* URL потока
## Установка
1. Импортируем шаблон Template App Flussonic Service API.xml в Zabbix
2. Добавляем к шаблон к узлу сервера Flussonic
3. На узле во вкладке макросы добавляем макросы авторизации пользователя {$FL.USER},{$FL.PASS} или изменяем "макросы узла сети и унаследованные" и указываем логин пароль (В бошинстве случаев достуточно указать макрос {$FL.PASS}). 
4. Через минуту шаблон обновит список потоков, еще через минуту соберет данные
