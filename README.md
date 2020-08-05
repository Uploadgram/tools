# uploadgram-tools
Some simple tools to interface with Uploadgram's API

### What you can find here
- [uploadgram_config.sxcu](https://github.com/Pato05/uploadgram-tools/blob/master/uploadgram_config.sxcu) — The simple configuration file for [ShareX](https://getsharex.com/) which could already be downloaded from [there](https://uploadgram.me/uploadgram_config.sxcu)
- [uploadgram_screenshot](https://github.com/Pato05/uploadgram-tools/blob/master/uploadgram_screenshot) — A simple bash script to make screenshots by using tools such as scrot, then upload it, copy it or save in a specific directory
  - For this to run you need the following dependencies:
    - deepin-screenshot/escrotum/maim/scrot — the core, tools to make screenshots, they are put in ease of use order
    - curl                                  — which is needed to make uploads
    - wc/du, awk                            — which usually come preinstalled
    - jq                                    — a simple command to parse json (needed for uploads)
    - libnotify                             — to get some status notifications
    - xclip                                 — to copy link/image to clipboard

### How to download uploadgram_screenshot
You can make a simple download by using
```bash
curl -O https://raw.githubusercontent.com/Pato05/uploadgram-tools/master/uploadgram_screenshot
```
But let's suppose you want to install it for the whole system (which is a common use case)
```bash
curl -s https://raw.githubusercontent.com/Pato05/uploadgram-tools/master/uploadgram_screenshot | sudo cat > /usr/bin/uploadgram_screenshot
```

### How to setup the tool for easy access
If you are on KDE Plasma, you can go onto `System Settings > Shortcuts > Custom Shortcuts` and set your own shortcut by going to `Edit > New > Global Shortcut > Command/URL`, then set your keyboard shortcut in the `Activation` tab and finally type `uploadgram_screenshot` inside the `Action` tab
