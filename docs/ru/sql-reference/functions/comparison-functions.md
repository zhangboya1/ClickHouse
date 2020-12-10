---
toc_priority: 36
toc_title: "\u0424\u0443\u043d\u043a\u0446\u0438\u0438\u0020\u0441\u0440\u0430\u0432\u043d\u0435\u043d\u0438\u044f"
---

# Функции сравнения {#funktsii-sravneniia}

Функции сравнения возвращают всегда 0 или 1 (UInt8).

Сравнивать можно следующие типы:

-   числа;
-   строки и фиксированные строки;
-   даты;
-   даты-с-временем;

внутри каждой группы, но не из разных групп.

Например, вы не можете сравнить дату со строкой. Надо использовать функцию преобразования строки в дату или наоборот.

Строки сравниваются побайтово. Более короткая строка меньше всех строк, начинающихся с неё и содержащих ещё хотя бы один символ.

Замечание. До версии 1.1.54134 сравнение знаковых и беззнаковых целых чисел производилось также, как в C++. То есть, вы могли получить неверный результат в таких случаях: SELECT 9223372036854775807 \> -1. С версии 1.1.54134 поведение изменилось и стало математически корректным.

## equals, оператор a = b и a == b {#function-equals}

## notEquals, оператор a != b и a `<>` b {#function-notequals}

## less, оператор `<` {#function-less}

## greater, оператор `>` {#function-greater}

## lessOrEquals, оператор `<=` {#function-lessorequals}

## greaterOrEquals, оператор `>=` {#function-greaterorequals}

[Оригинальная статья](https://clickhouse.tech/docs/ru/query_language/functions/comparison_functions/) <!--hide-->