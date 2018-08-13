# Summary
・gRPCはクライアント/サーバーからの単方向ストリーム、双方向ストリームをサポートしている  
・protoファイルから自動生成された構造体のSend/Recvメソッドによってストリームを操作することができる  
・ストリームからio.EOFが取得されたら送信側からのストリームが終了したことを意味する  
・ストリーミングの方式によって、RPC終了時にストリーム操作用の構造体に定義されたメソッドを実行する場合もある  

# Description
The route guide server and client demonstrate how to use grpc go libraries to
perform unary, client streaming, server streaming and full duplex RPCs.

Please refer to [gRPC Basics: Go](https://grpc.io/docs/tutorials/basic/go.html) for more information.

See the definition of the route guide service in routeguide/route_guide.proto.

# Run the sample code
To compile and run the server, assuming you are in the root of the route_guide
folder, i.e., .../examples/route_guide/, simply:

```sh
$ go run server/server.go
```

Likewise, to run the client:

```sh
$ go run client/client.go
```

# Optional command line flags
The server and client both take optional command line flags. For example, the
client and server run without TLS by default. To enable TLS:

```sh
$ go run server/server.go -tls=true
```

and

```sh
$ go run client/client.go -tls=true
```
