# sc1003-final-assignment-helper

`With compliments, Scott CJX`

PS. I like kopi peng. I accept googlepay, paynow, [paylah](./rsc/plspaylahme.jpg)

- @ [biz@carou](https://www.carousell.sg/p/programming-coding-help-consultation-1196819850/)
- @ [email: scottcjx.w@gmail.com](mailto:scottcjx.w@gmail.com)
- @ [tele: scjxw](https://t.me/scjxw)
- @ [github: scott-cjx](https://github.com/scott-cjx)

This assignment is programmed wholly in C, here are some functions that need to be implemented. 

## Required Functions
These functions are set as requirements for this assignment.

The requirements only very briefly mention what the functions should do. Here i shall give a most in-depth run-down of the requirements.

- [`listBooks()`](#listBooks)
- [`addBook()`](#addBook)
- [`removeBook()`](#removeBook)
- [`updateBook()`](#updateBook)
- [`findBook()`](#findBook)

## Helper Functions 
These functions are of MY own, that i used in my assignment. you ought to create your own.

- for: Menu 
    - `func: diplay menu`
    - `func: get user menu choice`
    - `func: run user menu choice`
- for: Book
    - `func: print book contents`
    - `func: add book to database`
    - `func: remove book from database`
    - `func: find book from database`
    - `func: case-insensitive string comparison`


### `listBooks()`
This function should list out all the books currently in the bookshop

1. print "listBooks():"
2. print "The bookshop is empty" if no books in database
3. print book contents for each book in database

### `addBook()`
This function should add a new book into the database

1. print "addBook():"
2. get user input for each of book features (id, title, author, etc.)
3. print "The bookshop is full! Unable to addBook()" if database is full, exit function
4. print "The bookID has already existed! Unable to addBook()" if book exists in database, exit function
5. add book with user input information to database


```
Note:
The is a requirement that the books are sorted by bookId within the database. 
Here are some ways in approaching this.

1. post processing:
-> add/remove book 
-> sort database

2. during processing:
-> find position of where book is/should be 
-> (for add:) 
-> -> shift the pointers of the books after target by +1 pos
-> -> add book to pos.
-> (for remove:) 
-> -> shift the pointers of the books after target by -1 pos
-> -> populate last position of database with empty book 
    (optional if there is a seperate counter for number of books)
```

### `removeBook()`
This function should remove a book in database (if exists) according to book information (title & author). You should write [findBook() function](#findbook) before this.

1. print "removeBook():"
2. get user inputs for title & author
3. search for and get the book from database.
4. print "The bookshop is empty" if database empty
5. print "The target book is not in the bookshop" if book not in database
6. remove book from database *
7. The target book is removed

\*`Note: refer to `[`addBooks note`](#addbook)


### `updateBook()`
This function should update a book in database (if exists) according to book information. You should write [findBook() function](#findbook) before this.

1. print "updateBook()"
2. get user inputs for title & author
3. search for and get the book from database.
4. print "The target book is not in the bookshop" if book not in database
5. get user inputs for "updated" price & quantity
6. update book in database

```
Note:
to update a book in database, here are some ways:
1. directly modify values on book in database (easiest)
2. use a buffer/temporary book, input all updated values 
    + original values (unchanged) -> replace book in database. 
```

### `findBook()`
This function should find a book in the database and inform the useer if the book exists or not. 

1. print "findBook():"
2. get user inputs for title & author
3. search for and get the book from database.
4. print "The target book is not found" if book not in database
5. print "The target book is found" if book in database

This function should use the following helper functions 
1. `func: case-insensitive string comparison` in `func: search book from database` to compare book information case-insensitively.
2. `func: search book from database` to search for the target book


## License
This project is available under the GPL v3 license. See the [LICENSE](./LICENSE.md) file for more info.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) 


