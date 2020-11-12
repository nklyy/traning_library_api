# Library API

Простое тренировочное API для библиотеки.

## API

* GET /book/:id - получить книгу по ее id
* GET /book/ - получить все книги, доступны параметры:
  * offset - оффсет(страница), по-умолчанию 0(первая страница)
  * limit - количество записей, по-умолчанию 1000
  * orderBy - сортировка по заданному полю, возможные значения:
    * id
    * title
    * date
    * author
    * description
    * image Пример: ?orderBy=title
  * groupBy - группировка по заданным полям. Пример: ?groupBy=title,author

* POST /book/ - добавить новую книгу, формат книги

```js
{
    "title": "some title",
    "author": "some author"
    "date": "some date",
    "description": "some description",
    "image": "some image"
}
```

* PUT /book/:id - обновление книги с заданным id

* DELETE /book/:id - удаление книги с заданным id
