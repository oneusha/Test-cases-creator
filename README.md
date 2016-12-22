# Test-cases-creator
Генератор документации тест-кейсов.


Для настройки полей пока используется JSON-формат. В дальнейшем планируется сделать интерфейс.
## Описание полей JSON

### Для шапки
```
{
    "rows": [ --- массив всех полей общей информации о тесте
        {
            "code": "name",  --- уникальный в рамках всех элементов массива "rows" код поля. Нигде не выводится. 
                                 Используется для служебных целей
            "colspan": 2, --- количество колонок в результирующей таблице для названия поля.
                              Может быть числом или процентами, например, 6 или '100%'.
            "width": "1%", --- ширина колонки в процентах для поля ввода значения
            "name": "Название", --- текст-название поля
            "inInputs": true, --- индикатор необходимости отображения в блоке ввода
            "inResult": true  --- индикатор необходимости отображения в результирующей таблице
        }
    ]
}
```

### Для полей
```
{
    "cells": [ --- массив всех полей общей информации о тесте
        {
            "code": "name",  --- уникальный в рамках всех элементов массива "cells" код поля. Нигде не выводится. 
                                 Используется для служебных целей
            "colspan": 2, --- количество колонок в результирующей таблице для поля.
                              Может быть числом или процентами, например, 6 или '100%'.
                              Сумма всех полей для всех типов (предусловия, шаги, постусловия) д.б. одинаковая
            "width": "1%", --- ширина колонки в процентах для поля ввода значения
            "name": "Название", --- текст-название поля. Используется в строке-заголовке блока и в качестве подсказки в поле ввода
            "inInputs": true, --- индикатор необходимости отображения в блоке ввода
            "inResult": true  --- индикатор необходимости отображения в результирующей таблице
        }
    ]
}
```
