### rpcx
---
https://github.com/smallnest/rpcx

```go
s := server.NewServer()
  s.RegisterName("Arith", new(example.Arith), "")
  s.Serve("tcp", addr)
  
d := client.NewPeer2PeerDiscoverty("tcp@"+addr, "")
  xclient := client.NewXClient("Arith", client.Failtry, client.RandomSelect, d, client.DefaultOption)
  defer xclient.Close()
  err := xclient.Call(context.Background(), "Mul", args, reply, nil)
  
  
```

```
go get -u -v -tags "reuseport quic kcp zookeeper etcd consul ping rudp utp" github.com/smallnest/rpcx/
```

```
```


