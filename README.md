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
r := room.New()
l := r.Logger()

r.OnPlayerJoin(func(p *room.Player) {
	l.Info("a player joined!")
})

r.OnPlayerLeave(func(p *room.Player) {
	l.Info("a player leaved!")
})

l.Infof("room link: %v", r.Link())
```
```json
# auto-generated config.json
{
  "Bot": {
    "Active": true,
    "Name": "Bot"
  },
  "General": {
    "Name": "My Room",
    "Token": "",
    "Debug": false,
    "MaxPlayer": 16
  },
  "Security": {
    "Public": false,
    "Password": ""
  }
}
```
