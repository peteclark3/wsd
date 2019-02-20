# wsd

> = **W**eb**S**ocket **D**ebugger

[![Build Status](https://travis-ci.org/alexanderGugel/wsd.svg?branch=master)](https://travis-ci.org/alexanderGugel/wsd)

![Terminal Demo](https://cdn.rawgit.com/alexanderGugel/wsd/demo/demo.gif)

Simple command line utility for debugging WebSocket servers.

## Installation

Via `go-get`:

```
$ go get github.com/peteclark3/wsd
```

## Usage

Command-line usage:

```
Usage of ./wsd:
  -help
      Display help information about wsd
  -insecureSkipVerify
      Skip TLS certificate verification
  -origin string
      origin of WebSocket client (default "http://localhost/")
  -protocol string
      WebSocket subprotocol
  -url string
      WebSocket server address to connect to (default "ws://localhost:1337/ws")
  -version
      Display version number```
  -headers (new in this fork)
      Custom headers to send with the connection request, format: `name1:value1;name2:value2`
```

## Why?

Debugging WebSocket servers should be as simple as firing up `cURL`. No need
for dozens of flags, just type 

```
wsd -url=ws://localhost:1337/ws
``` 

and you're connected.

Or to connect with a custom header: 
```
wsd -url=ws://localhost:1337/ws -headers=API_KEY:12345
```

## License

 MIT
