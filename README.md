# Go bookstore
A simple demo that helps you build bookstore api via golang


## Context
This demo comes from [bookstore](https://github.com/bigwhite/publication/tree/master/column/timegeek/go-first-course/09/bookstore) to promptly go through a golang with standard structure.

### Installation

- Analyze dependencies and versions to update go.mod

  ```
  go mod tidy
  ```

- Compile bookstore

  ```
  go build bookstore/cmd/bookstore
  ```

- Run bookstore

  ```
  ./bookstore
  2022/06/12 22:46:49 web server start ok
  2022/06/12 22:46:51 recv a POST request from 127.0.0.1:55380
  2022/06/12 22:47:22 recv a GET request from 127.0.0.1:55383
  2022/06/12 22:58:12 recv a GET request from 127.0.0.1:55451
  ```

### Test

- Post a new book item request

    ```
    curl -X POST -H "Content-Type:application/json" -d '{"id": "978-7-111-55842-2", "name": "The Go Programming Language", "authors":["Alan A.A.Donovan", "Brian W. Kergnighan"],"press": "Pearson Education"}' localhost:8080/book
    ```
- Get the book item info
    ```
    curl -X GET -H "Content-Type:application/json" localhost:8080/book/978-7-111-55842-2
    ```
