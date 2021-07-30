<h1 align="center">Haxballgo</h1>
<p align="center"><strong>Haxball headless API wrapper for Go</strong></p>

<p align="center">
  <a href="https://opensource.org/licenses/gpl-3.0.html">
    <img alt="License" src="https://img.shields.io/github/license/schphe/haxballgo?color=success&style=for-the-badge">
  </a>

  <a href="https://github.com/schphe/haxballgo/issues">
    <img alt="GitHub Issues" src="https://img.shields.io/github/issues/schphe/haxballgo?style=for-the-badge">
  </a>

  <a href="https://github.com/schphe/haxballgo/stargazers">
    <img alt="GitHub Stars" src="https://img.shields.io/github/stars/schphe/haxballgo?style=for-the-badge">
  </a>
</p>

## 💡 Simple usage

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
