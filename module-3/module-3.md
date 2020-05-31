## Модуль 3. «Загрузка и форматы данных (Data Ingestion)».

Описание:

По результатам модуля:

- грузим в файловую систему

- смотрим форматы

- сравниваем сжатия

- настраиваем репликацию


### Занятие 11. Распределенные файловые системы.

- Принципы работы распределенных файловых систем

- Структура кластера HDFS

- Тонкости настройки HDFS - конфигурация, защита, обеспечение отказоустойчивости


### Занятие 12. Инструменты выгрузки данных из сторонних систем - 1 часть.

- Типы систем-источников. Структурированные, полу- и неструктурированные данные. Логи, выгрузки из АС, Clickstream

- Инструменты для извлечения и загрузки данных - Flume, Sqoop, StreamSets, Fluentd, Debezium, logstash

- Практические примеры загрузки данных из сервисных баз данных


### Занятие 13. Очереди сообщений, Kafka, Confluent platform.

- Kafka, RabbitMQ

- Потоковая обработка (виды обработки, описание Producer–consumer problem, пример архитектурного решения через Kafka, RabbitMQ, NATS)

- Google Dataflow paper (Event time vs processing time и так далее). 

- Паттерны stream processing Joins, enricher, router. Event-sourcing.


### Занятие 14. Инструменты выгрузки данных из сторонних систем - 2 часть.

- Типы систем-источников. Структурированные, полу- и неструктурированные данные. Логи, выгрузки из АС, Clickstream

- Инструменты для извлечения и загрузки данных - Flume, Sqoop, StreamSets, Fluentd

- Практические примеры загрузки данных из сервисных баз данных


#### Домашнeе заданиe № 5. Создать снепшот аналитической таблицы из операционного хранилища.

1. Скопируйте на свою рабочую станцию (ПК или Google Cloud) данный репозиторий: https://github.com/renardeinside/vogel

2. Перейдите в папку проекта (vogel) и запустите все необходимые инстансы командой:

docker-compose up --build 

3. Сгенерируйте токен для доступа к Jupyter Notebook (выполните эту команду в проектной папке):

docker-compose -f docker-compose.yml exec jupyter-local jupyter notebook list

4. Перейдите в браузер и введите в нем полученную ссылку с токеном. 

5. В Jupyter Notebook перейдите в папку work, в ней откройте ноутбук postgres_snapshot. 

6. Запустите в нем все шаги до шага Read and join the data. 

7. В переменную query запишите select-запрос, который выводит следующие данные (доступные таблицы - customers, products, orders):

id - id пользователя из таблицы customers

first_name - first_name пользователя из таблицы customers

last_name - last_name пользователя из таблицы customers

total_weight - суммарный размер всех продуктов данного пользователя (поле weight в таблице products)

load_dttm - дата/время выполнения команды загрузки

Выполните данную ячейку командой Shift + Enter. 

Дополнительные ограничения запроса - необходимо выграть только тех пользователей, у которых id&lt;=1005. 

Информацию по структурам таблиц вы можете прочесть в README.md файле. 

8. Проверьте что были записаны верные данные в следующей ячейке. 

9. В комментарии к ДЗ пришлите ваш форк данного репозитория с верной sql-командой. 

_____________________________