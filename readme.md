## about
basic haxball room api for go

## usage

```
go get github.com/schphe/haxballgo@0.0.1
```

```go
func main() {
  r := room.New()
  defer r.Shutdown()
  
  l := r.Logger()
  s := r.Scheduler()

  r.OnPlayerJoin(func(p *room.Player) {
	  l.Infof("Player %v joined!", p.Name())
  })

  r.OnPlayerLeave(func(p *room.Player) {
	  l.Infof("Player %v leaved!", p.Name())
  })

  s.Repeating(time.Second, func(stop func()){
    r.Announce("Test message")
  })
}
```

```json
# auto-generated config.json
{
  "Bot": {
    "Active": false,
    "Name": "Bot"
  },
  "General": {
    "Name": "My Room",
    "Token": "",
    "MaxPlayer": 16
  },
  "Security": {
    "Public": true,
    "Password": ""
  },
  "Logging": {
    "Debug": false,
    "Pretty": true
  }
}
```
