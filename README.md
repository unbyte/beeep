## beeep
[![GoDoc](https://godoc.org/github.com/unbyte/beeep?status.svg)](https://godoc.org/github.com/unbyte/beeep) 
[![Go Report Card](https://goreportcard.com/badge/github.com/unbyte/beeep?branch=master)](https://goreportcard.com/report/github.com/unbyte/beeep) 

`beeep` provides a cross-platform library for sending desktop notifications, alerts and beeps.

> It's a fork form [https://github.com/gen2brain/beeep](https://github.com/gen2brain/beeep)
>
> This fork makes it possible to control App name (App id) on Windows. (It's default to `Powershell`)

### Installation

    go get -u github.com/gen2brain/beeep

### Examples

```go
err := beeep.Beep(beeep.DefaultFreq, beeep.DefaultDuration)
if err != nil {
    panic(err)
}
```

```go
err := beeep.Notify("Title", "Message body", "assets/information.png")
if err != nil {
    panic(err)
}
```

```go
err := beeep.Alert("Title", "Message body", "assets/warning.png")
if err != nil {
    panic(err)
}
```

To change App name on Windows
```go
beeep.AppID = "your app id"
```

## macOS

For icons to show up when using Alert() or Notify(), you will need to bundle your application
with a app icon.

## More

For cross-platform dialogs and input boxes see [dlgs](https://github.com/gen2brain/dlgs).
