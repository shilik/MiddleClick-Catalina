<div align="center">
  <h1>
    MiddleClick <img align="center" height="80" src="Images.xcassets/AppIcon.appiconset/mouse128x128.png">
  </h1>
  <p>
    <b>Emulate a middleclick with three finger Click or Tap on MacBook trackpad and Magic Mouse</b>
  </p>
  <p>
    with <b>macOS Catalina</b> <sup>10.15</sup> support!
  </p>
  <br>
</div>

##### It's useful:
> System-wide, you can close tabs by middleclicking on them.

> In Safari, middleclicking on a link opens it in background.

<br>

## Install

### Via [Homebrew Cask](//brew.sh) (Recommended)

```powershell
brew cask install dafuqtor/tap/midclick
```

### Direct Download

<details>
  <summary>
    <a href="//github.com/DaFuqtor/MiddleClick/releases/latest/download/MiddleClick.app.zip">
      Latest Release
    </a>&nbsp
    <a href="//github.com/DaFuqtor/MiddleClick/releases/latest">
      <img alt="GitHub release" src="https://img.shields.io/github/release/dafuqtor/middleclick?label=%20">
    </a>
  </summary>
  
  > Additionally, you may also view <a href="//github.com/DaFuqtor/MiddleClick/releases">Earlier Releases</a>
  
</details>

<br>

### Add Login Item

> Make it open automatically when you log in, it's handy to do using command line

```powershell
osascript -e 'tell application "System Events" to make login item at end with properties {path:"/Applications/MiddleClick.app", hidden:true}'
```

### Hide Status Bar Item

1. Holding <kbd>⌘</kbd>, drag it away from the status bar until you see a cross icon
2. Let it go

> To recover the item, just open MiddleClick when it's already running

---

<details>
  <summary>This fork differs from the <a href="//github.com/cl3m/MiddleClick">base fork</a> in some ways</summary>

- Configuration: Click or Tap
  - preferred setting is saved for every user
- Removed old 32-bit/PowerPc `relaunch` binary due to it's incompatibility with macOS 10.15 Catalina and greater. Replaced with inline restarting of the app
- The App will not only restart on waking the Mac, but when a new touch device is added (so it immediately gains middleclicking ability) and when a display is added/reconfigured (which seems to be necessary)

</details>

#### Attention! Make sure to:

1. Quit an old version of MiddleClick
2. Remove it from the privacy settings
3. Enable the new version in privacy settings when prompted

> It is important to follow the steps in order, otherwise the Mouse may not be clickable and you have to `killall MiddleClick` via terminal or even force reset the Mac.
