---
layout: post
title: "Installing Go by Homebrew on Mac OS X"
date: 2015-06-21 08:29:53 +0900
comments: true
categories: Go
---


## Install go by brew

Install golang by brew. I think that's the easiest way to install go on OS X.


```
$ brew install go
==> Downloading https://downloads.sf.net/project/machomebrew/Bottles/go-1.4.yosemite.bottle.ta
######################################################################## 100.0%
==> Pouring go-1.4.yosemite.bottle.tar.gz
==> Caveats
As of go 1.2, a valid GOPATH is required to use the `go get` command:
  http://golang.org/doc/code.html#GOPATH

`go vet` and `go doc` are now part of the go.tools sub repo:
  http://golang.org/doc/go1.2#go_tools_godoc

To get `go vet` and `go doc` run:
  go get golang.org/x/tools/cmd/vet
  go get golang.org/x/tools/cmd/godoc

You may wish to add the GOROOT-based install location to your PATH:
  export PATH=$PATH:/usr/local/opt/go/libexec/bin
==> Summary
?  /usr/local/Cellar/go/1.4: 4557 files, 134M
```



## Set Path for Go

Go needs paths for his root directory. I wrote like that.


```
# .zshrc
# go
export GOROOT=/usr/local/opt/go/libexec
export GOPATH=$HOME/.go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
```

It is actually religious problems how people set `$GOPATH` and `$GOROOT`. Let you set them up to your belief. 


## Run Tiny Program

To test, run tiny program of Hello World.

```
~/workspace
▶ vi hello.go
```

```go
// hello.go
package main
import "fmt"

func main() {
  fmt.Printf("Hello, world!")
}
```

```
~/workspace
▶ go run hello.go
Hello, world!%
```

Now it's working well! 

Next time, I will make a command tool or http server in Go.

Maybe it is not good idea to web application in Go right...?

