# HackNU

### Мы предоставляем тестовые данные. Две таблицы закупок и продаж (`supply`, `sale`):
1. Таблица закупок (`supply`) с колонками:
    - `id`
    - `barcode`
    - `quantity`
    - `price`
    - `time`
2. Таблица продаж (`sale`) с колонками:
    - `id`
    - `barcode`
    - `quantity`
    - `price`
    - `time`
#### Тестовые данные находятся [здесь](https://some-link.com/).

### Вам нужно написать ([REST API](https://habr.com/ru/articles/483202/)) методы для:
#### 1. [Cоздания, редактирования, удаления и просмотра закупа](https://umaghacknu.docs.apiary.io/#reference/0/0/0).
#### 2. [Cоздания, редактирования, удаления и просмотра продажи](https://umaghacknu.docs.apiary.io/#reference/0/1/0).
#### 3. [Подсчета прибыли за период с учетом себестоимости по FIFO](https://umaghacknu.docs.apiary.io/#reference/0/2/0).
- Через REST закупы и продажи можно создавать, редактировать, удалять. Редактируемые поля: `кол-во`, `цена`, `время`. Можно создавать закуп и продажу задним числом.
- Себестоимость подсчитывается/пересчитывается при создании, редактировании, удалении продажи и закупок по методу [FIFO (First in first out)](https://ru.wikipedia.org/wiki/FIFO_%D0%B8_LIFO).

### Как проверить правильность REST запросов:
#### Тут будет интсрукция по тому, как проверить правильность REST запросов через Postman коллекции.


# Как определяется победитель?
1. Подсчет прибыли должен быть правильным. Нужно описать (или нарисовать) алгоритм подсчета.
2. Алгоритм подсчета должен быть эффективным.

### Подсказка 1:
Можно добавить колонку margin в продаже или хранить в отдельной таблице.

### Подсказка 2:
В приоритете будут рассматриваться алгоритмы подсчета себестоимости с меньшим количеством итерации и с меньшим объемом памяти (RAM и жесткий диск).
