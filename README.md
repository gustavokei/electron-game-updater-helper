# Electron Game Updater Helper
![](https://i.imgur.com/2fxPONJ.gif)

This portable Windows app is supposed to be used with [gustavokei/electron-game-updater](https://github.com/gustavokei/electron-game-updater)

* Generates an update list JSON file (see egu-update-list.json) with data of all files within its directory
* Highly customizable (see eguh-config.json)

If you don't want to compile it, [check out the releases page](https://github.com/gustavokei/electron-game-updater-helper/releases)

## egu-config.json example

* `url` = direct download url
* `specialFiles` = files that will have an [unique hash](https://nodejs.org/api/crypto.html#crypto_crypto_createhash_algorithm_options)
* `ignoredFiles` = files that won't be included in the output file (for files in a subdir, do `subdir/file`)
* `output` = name of the output file
```json
{
  "url": "https://storage.googleapis.com/gc-client/",
  "specialFiles": ["main.exe", "stage/script.kom", "stage/char_script.kom"],
  "ignoredFiles": [
    "Electron-Game-Updater-Helper.exe",
    "Electron Game Updater Helper.exe",
    "egu-config.json"
  ],
  "output": "egu-update-list.json"
}
```

## egu-update-list.json example
```json
{
  "file": "main.exe",
  "size": 16637952,
  "hash": "kuc4HCv3bX7LCaRrloP4v2TjYpc=",
  "url": "https://storage.googleapis.com/gc-client/main.exe"
}
```
