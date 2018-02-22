# hello-world
Just another repository
Just another branche

```
<?php

function test() {
  console.log("notice the blank line before this function?");
}

```

## Components

An component is a simple array with some page data:

```
array(
	'page_number' => 2
	'url' => '//www.example.com/?page=2',
	'is_current' => false,
	'is' => 'next'
)
```

There are 6 possible components available via their methods:
1. getFirstPage(): to get data of the first page. There's always a first page available.
2. getPrevPage(): to get the previous page. Previous is not available on the first page, because there is no previous page.
3. getCurrentPage(): to get data of the current page. Always available.
4. getAdjacentPages(): to get an array with data of the adjacent pages. This is an optional component.
5. getNextPage(): to get data of the next page. Next is not available on the last page, because there is no next page.
6. getLastPage(): to get data of the last page. There's always a last page available.

Use the method getPageCollection() to get an array with all the components at once.

## Installation

Install with composer:

```
$ composer require ...
```

## Sql query example

An example to paginate database results.

```
$limit = $pagination->itemsPerPage;
$offset = $pagination->itemsOffset;
$sql = "SELECT * FROM {$table} LIMIT {$limit} OFFSET {$offset}";
```


  some other text

- item 1
- item 2
- item 3
  - item 3.1
  - item 3.2

