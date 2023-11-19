# Getting started Connect

connpass のイベントに参加した際に、講義で Connect を使用することになったため、事前に取り組んだ Getting started のソースコードです。

## How to use

リポジトリをローカルに用意する

```
git clone git@github.com:HarukiIdo/connect-go-example.git
```

いくつかのコード生成ツールをインストールする

```
go install github.com/bufbuild/buf/cmd/buf@latest
go install github.com/fullstorydev/grpcurl/cmd/grpcurl@latest
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install connectrpc.com/connect/cmd/protoc-gen-connect-go@latest
```

Go のインストール ディレクトリをパスに指定する

```
[ -n "$(go env GOBIN)" ] && export PATH="$(go env GOBIN):${PATH}"
[ -n "$(go env GOPATH)" ] && export PATH="$(go env GOPATH)/bin:${PATH}"
```

Connect サーバを立ち上げる

```
go run ./cmd/server/main.go
```

Connect クライアントから Connect サーバにリクエストを送る

```
go run ./cmd/client/main.go
```

## URLs

connpass: https://knowledgework.connpass.com/event/298684/

Docs: https://connectrpc.com/docs/go/getting-started#prerequisites

GitHub: https://github.com/connectrpc
