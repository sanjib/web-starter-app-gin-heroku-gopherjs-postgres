# web-starter-app-gin-heroku-gopherjs-postgres

## Tech Stack

1. Go
    - Gin
    https://github.com/gin-gonic/gin
    - GopherJS 
    https://github.com/gopherjs/gopherjs
2. Postgres Database
3. Heroku

## Running

### Windows

- For development in cmd prompt, ```set PORT=5000```
- Check if PORT has been set ```echo %PORT%```

### Any Platoform
- Build ```go build```
- Run the app ```web-starter-app-gin-heroku-gopherjs-postgres.exe```
- Point browser to http://localhost:5000/

## Development

1. Install Go
2. Install Git
3. Install Gin 
```go get -u github.com/gin-gonic/gin```
3. Install GopherJS 
```go get -u github.com/gopherjs/gopherjs```
4. Create Heroku Account
5. Install Heroku CLI 
https://devcenter.heroku.com/articles/heroku-cli#download-and-install

#### Go Module Setup
```
go mod init
go build
go mod vendor
```