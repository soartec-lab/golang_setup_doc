# Summary

This is a document to setup the following golang development environment

* Go
* beego
* SublimeText3 packages

## Enviroment
### OS version
Ubuntu 18.04.1 LTS

### Editor
SublimeText3

# Setup

## golang
### Install

See: https://github.com/golang/go/wiki/Ubuntu

```
$ sudo apt-get update
$ sudo apt-get install golang-go
```

### Export environment variable

```.bashrc
$ echo export GOPATH='$HOME/go' >> ~/.bashrc
$ echo export PATH='$PATH:/usr/lib/go-1.10/bin' >> ~/.bashrc
$ echo export PATH='$PATH:$GOPATH/bin' >> ~/.bashrc
$ source ~/.bashrc
```

Note: Do not forget reload command

### Install check

```
$ go version
$ go env
```

## beego

```
$ go get -u github.com/astaxie/beego
$ go get -u github.com/beego/bee
```

## SublimeText3

### tools

```
go get -u -v golang.org/x/tools/cmd/goimports
go get -u -v github.com/nsf/gocode
go get -u -v github.com/rogpeppe/godef
go get -u -v golang.org/x/tools/cmd/oracle
go get -u -v github.com/golang/lint/golint
```

### Sublime Package

Preferences > Package Control: Install Package

Note: short cut is `ctrl + shift + p`

install `Gotools` and `Golang Build`

#### Update Gotools setting

Preferences >　Package Settings > GoTools > Settings - Users

```
{
  "gopath": "/path/to/go",
  "format_backend": "both"
}
```

#### Update Golang Build setting

Preferences > Package Settings > Golang Config > Settings - User

```
{
  "GOPATH": "/path/to/go",
  "PATH:": "/path/to/go/bin"
}
```

#### Update key bind

Preferences > Key Bindings - User

```
[
  { "keys": ["super+d"], "command": "gotools_goto_def" },
]
```

