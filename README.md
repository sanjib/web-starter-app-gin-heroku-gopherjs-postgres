# web-starter-app-gin-heroku-gopherjs-postgres

Based on the tutorial "Go web app starter guide - Gin, Heroku, GopherJS, Postgres" by Brian Will: https://www.youtube.com/watch?v=uey7jIEmR3A

## App Published at Heroku

Home Page: https://web-app-gin-gopherjs-postgres.herokuapp.com

![hello world home page](./screenshots/hello-world.png)

![javascript console output from gopherjs](./screenshots/console.png)

![go code in browser console](./screenshots/go-code-in-browser-sources.png)

Database Test page: https://web-app-gin-gopherjs-postgres.herokuapp.com/tick

![database test page](./screenshots/tick.png)

## Tech Stack

1. Go
    - Gin
    https://github.com/gin-gonic/gin
    - GopherJS 
    https://github.com/gopherjs/gopherjs
2. Postgres Database
    - https://github.com/lib/pq
3. Heroku

## Running

### Windows

- For development in cmd prompt, ```set PORT=5000```
- Check if PORT has been set ```echo %PORT%```
- ```set DATABASE_URL=postgres://skezehaabtkfki:655df4f74465080a6f8ad57e4d688e43cd950999797f86239026dd19dbade6fc@ec2-54-83-1-101.compute-1.amazonaws.com:5432/dc61vlcgktmmji```

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
6. Install PosgreSQL driver ```go get github.com/lib/pq```

#### Go Module Setup
```
go mod init
go build
go mod vendor
```

#### Heroku

App: https://web-app-gin-gopherjs-postgres.herokuapp.com/

Database: postgresql-concentric-60467

DATABASE_URL: postgres://skezehaabtkfki:655df4f74465080a6f8ad57e4d688e43cd950999797f86239026dd19dbade6fc@ec2-54-83-1-101.compute-1.amazonaws.com:5432/dc61vlcgktmmji

```
heroku login
heroku create web-app-gin-gopherjs-postgres
git push heroku master
heroku addons:create heroku-postgresql:hobby-dev
heroku config:get DATABASE_URL -a web-app-gin-gopherjs-postgres
```