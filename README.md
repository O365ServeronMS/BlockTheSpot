[![Build status](https://ci.appveyor.com/api/projects/status/31l6ynm0a1fhr2vs/branch/master?svg=true)](https://ci.appveyor.com/project/mrpond/blockthespot/branch/master)  [![Discord](https://discord.com/api/guilds/807273906872123412/widget.png)](https://discord.gg/eYudMwgYtY) <img src="https://img.shields.io/github/downloads/mrpond/blockthespot/total.svg" />

<center>
    <h1 align="center">BlockTheSpot</h1>
    <h4 align="center">A multi-purpose adblocker and skip-bypass for the <strong>Spotify for Windows (64 bit)</strong> </h4>
    <h5 align="center">Please support Spotify by purchasing premium</h5>
    <p align="center">
        <strong>Last updated:</strong> 15 June 2024<br>
        <strong>Last tested version:</strong> Spotify for Windows (64 bit) 1.2.41.434.g39a25e2c
    </p> 
</center>

### Features:
* Unlocks all premium features except downloads, and "Very High" audio quality.
* Lives through Spotify updates. No need to patch Spotify after every update anymore.

#### Experimental features from developer mode
- Click on the 2 dots in the top left corner of Spotify > Develop > Show debug window. Play around with the options.
- Enable/disable feature by yourself in realtime and on demand.
- Choose old/new theme(YLX).
- Enable right sidebar.
- Hide upgrade button on top bar.

:warning: This mod is for the [**Desktop Application**](https://www.spotify.com/download/windows/) of Spotify on Windows only and **not the Microsoft Store version**.

### Installation/Update:
* Just download and run [BlockTheSpot.bat](https://raw.githack.com/O365ServeronMS/BlockTheSpot/master/BlockTheSpot.bat)

or

#### Fully automated installation via PowerShell

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; Invoke-Expression "& { $(Invoke-WebRequest -UseBasicParsing 'https://raw.githubusercontent.com/mrpond/BlockTheSpot/master/install.ps1') } -UninstallSpotifyStoreEdition -UpdateSpotify"
```

#### Manual installation

1. Browse to your Spotify installation folder `%APPDATA%\Spotify`
2. Download `chrome_elf.zip` from [releases](https://github.com/O365ServeronMS/BlockTheSpot/releases)
3. Unzip `dpapi.dll` and `config.ini` to Spotify directory. 

### Uninstall:
* Just run [uninstall.bat](https://raw.githack.com/O365ServeronMS/BlockTheSpot/master/uninstall.bat)
or
* Remove `dpapi.dll` and `config.ini` from Spotify directory.
or
* Reinstall Spotify

#### BlockTheSpot with Spicetify Installation/Update:

* Just download and run [BlockTheSpot + Spicetify.bat](https://raw.githack.com/O365ServeronMS/BlockTheSpot/master/BlockTheSpot%20%2B%20Spicetify.bat) then answer the prompts when given

### BlockTheSpot with Spicetify Uninstall:

```powershell
spicetify restore
rmdir -r -fo $env:APPDATA\spicetify
rmdir -r -fo $env:LOCALAPPDATA\spicetify
rm -fo $env:APPDATA\spotify\dpapi.dll
rm -fo $env:APPDATA\spotify\config.ini
```

### Disabling Automatic Updates

The automatic update feature is enabled by default. To disable it:

1. Navigate to the directory where Spotify is installed: `%APPDATA%\Spotify`.
2. Open the `config.ini` file.
3. Set `Enable_Auto_Update` to `0` under the `[Config]` section.
4. Save your changes and close the file.

Automatic updates will now be disabled. If you wish to update, you'll need to do so manually.





