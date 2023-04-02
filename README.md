# About
connectをhello worldをしました。（周辺知識も）

- connect
- buf

# Ref

- [次世代gRPC?『connect-go』やってみた](https://zenn.dev/rai_wtnb/articles/e07ad831ea8e34)
- [Buf tutorial](https://buf.build/docs/tutorials/getting-started-with-buf-cli/)

# App

## run
```
go run ./cmd/server/main.go
```

## sample request
### http
```
curl "http://localhost:8080/greet.v1.GreetService/Greet" -H 'Content-Type: application/json' -d '{"name": "rai"}'
{"greeting":"Hello, rai!"}%
```

### grpc
```
echo '{ "name": "rai" }' | evans -r -p 8080 cli call greet.v1.GreetService.Greet

{
  "greeting": "Hello, rai!"
}
```

# Connect


# Buf

## set up

```
buf mod init
```

## generate
- [doc](https://buf.build/docs/reference/cli/buf/generate#description)

```
buf generate --path=greet/v1
```

## build

```
buf build
```
