# golang+echo Webserver

## Start

```golang
go mod init github.com/CKjapan/{projectName}
```

```golang
go get github.com/labstack/echo
```

```bash
touch server.go
```

```golang
package main

import (
	"net/http"

	"github.com/labstack/echo"
)

func main() {
	e := echo.New()
	e.GET("/", func(c echo.Context) error {
		return c.String(http.StatusOK, "こんにちは!")
	})
	e.Logger.Fatal(e.Start(":1323"))
}
```


```golang
go run server.go
```

## Link

[Golang の echo を使う](https://qiita.com/ekzemplaro/items/5e89db529672523531c4)

[GolangとEchoでお手軽にAPIサーバを立てる](https://ken-aio.github.io/post/2019/01/30/golang-echo/)
