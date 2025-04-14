# Syncthing CLI guide
## Pairing Syncthing between Android and Linux CLI
- Install Syncthing
`apk add syncthing`
- Generate device ID, config files and default folder
`syncthing generate`
- Start Syncthing
`syncthing`
- Add Android device ID
`syncthing cli config devices add --device-id <android device id>`
- Accept pairing request on Android
- Share default folder with Android
`syncthing cli config folders default devices add --device-id <android device id>`
## Pairing Syncthing between Linux CLI and Linux CLI
- Get the device ID
`syncthing cli config devices add --device-id <android device id>`
- Accept default folder from Machine A
`syncthing cli config devices <android device id> auto-accept-folders set true`
[Syncthing CLI Setup Reference](https://gist.github.com/Jonny-exe/9bad76c3adc6e916434005755ea70389)
