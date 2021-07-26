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

r.OnPlayerJoin(func(p room.Player) {
	println("a player joined!")
})

r.OnPlayerLeave(func(p room.Player) {
	println("a player leaved!")
})


println("room link:", r.Link())
```
