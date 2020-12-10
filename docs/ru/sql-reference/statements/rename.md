---
toc_priority: 48
toc_title: RENAME
---

# RENAME {#misc_operations-rename}

Переименовывает одну или несколько таблиц.

``` sql
RENAME TABLE [db11.]name11 TO [db12.]name12, [db21.]name21 TO [db22.]name22, ... [ON CLUSTER cluster]
```

Переименовывание таблицы является лёгкой операцией. Если вы указали после `TO` другую базу данных, то таблица будет перенесена в эту базу данных. При этом, директории с базами данных должны быть расположены в одной файловой системе (иначе возвращается ошибка). В случае переименования нескольких таблиц в одном запросе — это неатомарная операция,  может выполнится частично, запросы в других сессиях могут получить ошибку `Table ... doesn't exist...`.


[Оригинальная статья](https://clickhouse.tech/docs/ru/sql-reference/statements/rename/) <!--hide-->