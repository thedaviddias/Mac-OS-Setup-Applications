# My Mac OS setup and workflow

## Table of content

[TOC]

## My Hardware

Computer: 13" Late 2017 Macbook Pro with Touch bar.

Monitor: [LG 34UM69G-B 34" 21:9 UltraWide](https://www.amazon.ca/gp/product/B06XFXX5JH/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

Keyboards:

* At Work: [Pock3R](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=3631) black with blue leds
* At Home: [Ducky One 2 RGB TKL](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=4284)

Mouses:

* 2 [Logitech MX Master 2S](https://www.amazon.ca/dp/B071YZJ1G1/ref=cm_sw_em_r_mt_dp_U_92mNEbX6PD4H0)

Accessories:

* [Elgato Stream Deck](https://www.amazon.ca/dp/B06XKNZT1P/ref=cm_sw_em_r_mt_dp_U_64mNEbDTVAA81)
* [Elgato Green Screen](https://www.amazon.ca/dp/B0743Z892W/ref=cm_sw_em_r_mt_dp_U_n-mNEbNJ37DDK)
* [Focusrite Scarlett-2i2 Gen2](https://www.amazon.ca/dp/B005OZE9SA/ref=cm_sw_em_r_mt_dp_U_v7mNEb9RZNDFG)
* [DBX 286s Microphone Pre-amp Processor](https://www.amazon.ca/dp/B004NDFRVC/ref=cm_sw_em_r_mt_dp_U_V7mNEbTJ0E20E)
* Rode Procaster

## Setup shell



#### Install [Homebrew](https://brew.sh)

```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
#### Install [Caskfile]()

```bash
brew install caskroom/cask/brew-cask
```

or brew tap caskroom/cask?

brew cask install cakebrew
https://www.cakebrew.com/

#### Install [ZSH]()

```bash
brew install zsh
```

Add this to my `./zshrc`

```
export HOMEBREW_CASK_OPTS="--appdir=/Applications"
```

#### Install [Oh My Zsh]()

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Check if Oh My Zsh was correctly installed

```bash
zsh --version
```

Add spaces to my dock 

```sh
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'; killall Dock
```


```sh
 brew update                           # Fetch latest version of homebrew and formula.
$ brew tap caskroom/cask                # Tap the Caskroom/Cask repository from Github using HTTPS.
$ brew search {app name}                    # Searches all known Casks for a partial or exact match.
$ brew cask info {app name}                # Displays information about the given Cask
$ brew cask install {app name}             # Install the given cask.
$ brew cleanup   
```


brew tap homebrew/cask-fonts
brew install wget
brew install ffmpeg
brew install youtube-dl
brew install imagemagick

## Command Line Apps

nvm

ruby

- [yarn](https://github.com/yarnpkg/yarn) - Fast, reliable, and secure dependency management.



#### GNU Coreutils
```sh
brew install coreutils
```

#### MAS - Install App Store apps from the command line
```sh
brew install mas
```

mas search app name

#### Act - Run Github Actions Locally
```sh
brew install nektos/tap/act
```

#### Github CLI
```sh
brew install github/gh/gh
```


## Applications

This is a complete list of all the applications I have on my personal and professional Mac (some apps are only on my personal computer).

 [Xcode]() - 
![Free][licence-free] ![Usage low][usage-low]

- Xcode is required for some applications to run. So having Xcode updated just remove the issue of not being able to install some apps.

### The minimum essential

This is the list of the most essentials apps I would install if I was limited in the number of apps to have.

<img src="media/15878421335213.jpg" width="50" align="right">

#### [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html) - Control incoming/outgoing network traffic
![Licence ~$30][licence-30] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install little-snitch
```

<img src="media/15878412922030.png" width="50" align="right">

#### [1Password](https://1password.com) - Password manager
![Yearly subscription][subscription-yearly] ![Proprietary backup][backup-proprietary] ![High usage][usage-high]

- Generate all of my passwords with it and keep everything in a secured and encrypted vault kept secure by my one master password.
- No longer need to remember passwords and I now have a unique password for every website that I am signed up on whilst [activating two factor authentication](https://support.1password.com/one-time-passwords/) wherever possible.
- All my applications licences are saved in 1Password
- I switched from using LastPass in 2019

##### CLI installation
```sh
brew cask install 1password

mas install 1333542190
```

<img src="media/15878422056701.jpg" width="50" align="right">

#### [Alfred 4](https://www.alfredapp.com) - Launcher, the best alternative for Spolight
![Free][licence-free-limit] ![Licence ~$30][licence-30] ![Backup Dropbox][backup-dropbox] ![High usage][usage-high]

- **Snippets**: previously using [TextExpander](https://textexpander.com/), I switched in using the snippet feature in Alfred. (text-expander to aflred)

- Workflows used (files saved on Dropbox):
    - [caniuse](https://github.com/willfarrell/alfred-caniuse-workflow)
    - [DEVONThink Search](https://www.packal.org/workflow/devonthink-search)
    - F.lux
    - Lorem Ipsum
    - MDN Search
    - Snippets Lab
    - Spotify Mini Player
    - Things
    - Alfred Maestro

##### CLI installation
```sh
brew cask install alfred
```

#### [iTerm2](https://www.iterm2.com/downloads.html) - 
![Free][licence-free]

##### CLI installation
```sh
brew cask install iterm2
```


<img src="media/15878423395361.png" width="50" align="right">

#### [Spotify](https://www.spotify.com/) - Music
![Montly subscription][subscription-montly] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install spotify
```

### Browsers
![Free][licence-free]


#### [Google Chrome](https://www.google.com/chrome/)

Multiple profiles
- Professional user
- Personnal user
- Accessibility user

##### CLI installation
```sh
brew cask install google-chrome
```

##### Extensions
* Feedly Mini
* Adblock Plus
* 1Password
* Toolbar Spacer
* Clip to DEVONthink
* Save to Notion
* Add to Things 3
* Eagle

#### [Google Chrome Canary](https://www.google.com/chrome/canary/)

##### CLI installation
```sh
brew cask install google-chrome-canary
```

#### [Firefox](https://www.mozilla.org/en-CA/firefox/new/)

##### CLI installation
```sh
brew cask install firefox
```

#### [Firebox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/)

##### CLI installation
```sh
brew cask install firefox-nightly
```

#### [Microsoft Edge](https://www.microsoft.com/en-us/edge) - The browser from Microsoft

##### CLI installation
```sh
brew cask install microsoft-edge
```

### Utilities

#### [Bartender 3](https://www.macbartender.com/) - Organize menu bar icons
![Licence ~$20][licence-20] ![High usage][usage-high]

##### Screenshots

- Show view

- Hide view

##### CLI installation
```sh
brew cask install bartender
```

#### [Flux](https://justgetflux.com/)
![Free][licence-free] ![Usage high][usage-high] [![Show your support][support]](https://justgetflux.com/promo/paypal2.html)

##### CLI installation
```sh
brew cask install flux
```

#### [PopClip](https://pilotmoon.com/popclip/) - Giving more power to my mouse
![Licence ~$10][licence-10] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install popclip
```

- List of [extensions I use](https://pilotmoon.com/popclip/extensions/)

#### [Contexts](https://contexts.co) - Window switcher
![Licence ~$10][licence-10] ![Usage high][usage-high]

- Shortcut used:
    ctrl + space

##### CLI installation
```sh
brew cask install contexts
```

#### [Kap](https://getkap.co/) - An open-source screen recorder
![Free][licence-free] ![Usage high][usage-high]


- Plugins activated: 
    - [Kap Dropbox](https://github.com/karaggeorge/kap-dropbox)

##### CLI installation
```sh
brew cask install kap
```

#### [CleanMyMac X](https://macpaw.com/cleanmymac) - To maintain my Mac as he was new
![Licence ~$50][licence-50] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install cleanmymac
```

#### [Muzzle](http://muzzleapp.com) - Silence embarrassing notifications
![Free][licence-free] ![Usage high][usage-high]

#### [Lungo](https://sindresorhus.com/lungo) - Prevent your Mac from going to sleep
![Free][licence-free] ![Usage medium][usage-medium]

#### [Stream Deck](https://www.elgato.com/en/gaming/downloads) - 
![Usage medium][usage-medium]

##### CLI installation
```sh
brew cask install elgato-stream-deck
```

#### [Noizio](https://noiz.io/) - 
![Free][licence-free] ![Usage low][usage-low]

##### CLI installation
```sh
brew cask install noizio

mas install 928871589
```

#### [Mouseless](https://mouseless.app/) - 
![Licence ~$20][licence-20] ![Usage low][usage-low]

#### [TeamViewer](https://www.teamviewer.com/en/) - 
![Free][licence-free] ![Usage low][usage-low]

I only use TeamViewer when I need to debug or help my Mom's computer.

#### [Cardhop](https://flexibits.com/cardhop)
![Licence ~$30][licence-30] ![Usage low][usage-low]

### Automation

#### [Keyboard Maestro](https://www.keyboardmaestro.com/main/) - The most powerful option to automate EVERYTHING on Mac
![Usage high][usage-high] ![Backup Dropbox][backup-dropbox]

#### [Hazel](https://www.noodlesoft.com/) - Automate repetitive tasks in a few clicks
![Licence ~$30][licence-30] ![Usage high][usage-high]

#### [Karabiner]() - Personalize keyboards
![Free][licence-free] ![Usage medium][usage-medium]

#### [BetterTouch Tool](https://folivora.ai/) - 
![Licence ~$30][licence-30]

#### [Hammerspoon](https://www.hammerspoon.org/) - OSX automation using Lua 
![Free][licence-free]

### Task management / tracking

#### [Fantastical](https://flexibits.com/fantastical) - Calendar
![Free][licence-free] ![High usage][usage-high]

- I use the app to manage personal and professional events.
- I always view my events from `Week` view. And show 5 days with 16h shown for all days. This lets me have a perspective over what I have to do now. What deadlines I have to complete soon. And gives me the freedom to adjust my schedule in light of upcoming deadlines and events.

##### CLI installation
```sh
brew cask install fantastical
```

#### [Things](https://culturedcode.com/things/) - Task manager
![Licence ~$30][licence-30] ![Proprietary backup][backup-proprietary] ![High usage][usage-high]

- I used [Todoist](https://todoist.com/) few years, low subscription and

##### CLI installation
```sh
brew cask install things
```

#### [Timing](https://timingapp.com/?lang=en) - To record everything I do without manual action
![Yearly subscription][subscription-yearly] ![High usage][usage-high]

##### CLI installation
```sh
brew cask install timing
```

### Storage / backup management

#### Dropbox - 
![Monthly subscription][subscription-montly] ![Usage high][usage-high]

- [ ] Select `Apps` and `Screenshots` folders to sync

##### CLI installation
```sh
brew cask install dropbox
```

#### Google Drive Backup Up
![Usage high][usage-high]

#### ForkLift - Dual pane file manager and file transfer client for macOS
![Licence ~$30][licence-30] ![Usage medium][usage-medium]

##### CLI installation
```sh
brew cask install forklift
```

#### [The Unarchiver]() - 
![Usage high][usage-high]

##### CLI installation
```sh
brew cask install the-unarchiver

mas install 425424353
```

#### Hard Disk Manager

GoodSync

### Code
----

#### [Visual Studio Code](https://github.com/Microsoft/vscode) - Code editor
![Free][licence-free] ![Usage high][usage-high]

sync settings

##### CLI installation
```sh
brew cask install visual-studio-code
```

#### [Tower](https://www.git-tower.com/) - Git client
![Yearly subscription][subscription-yearly] ![Usage high][usage-high]

aliases

##### CLI installation
```sh
brew cask install tower
```

#### Diffmerge
![Free][licence-free] ![Usage low][usage-low]

##### CLI installation
```sh
brew cask install diffmerge
```

#### [SnippetsLabs](https://www.renfei.org/snippets-lab/) - Code snippets manager
![Licence ~$10][licence-10] ![Backup iCloud][backup-icloud] ![Usage high][usage-high]

- I store all my code snippets 

Other options
- Alfred, VSCode

##### CLI installation
```sh
brew cask install little-snitch
```

#### [Proxyman](https://proxyman.io/) - Best Web Debugging Proxy for MacOS
![Free][licence-free-limit] ![Usage medium][usage-medium]

I found Proxyman when struggling making Charles working on my Mac. Proxyman make it really easy to....

#### [Paw](https://paw.cloud/) - HTTP client
![Backup Dropbox][backup-dropbox] ![Usage medium][usage-medium]

https://paw.cloud/extensions/

##### CLI installation
```sh
brew cask install paw
```

#### Postman
![Free][licence-free] ![Usage medium][usage-medium]

#### [Trailer](http://ptsochantaris.github.io/trailer/) - Github Notifications
![Free][licence-free] ![Usage high][usage-high]

#### [Mockoon](https://mockoon.com/)
![Free][licence-free] ![Usage medium][usage-medium]

##### CLI installation
```sh
brew cask install mockoon
```

#### [Docker](https://www.docker.com/products/docker-desktop) - 
![Free][licence-free] ![Usage high][usage-high]

##### CLI installation
```sh
brew install docker
```

#### [GraphQL Playground](https://github.com/prisma-labs/graphql-playground) - Another GraphQL IDE

##### CLI installation
```sh
brew cask install graphql-playground
```

#### [Altair GraphQL Client]() - Beautiful GraphQL Client
![Free][licence-free] [![Show your support][support]](https://opencollective.com/altair/donate)

##### CLI installation
```sh
brew cask install altair-graphql-client
```

#### [Screaming Frog SEO Spider]() - 
![Free][licence-free-limit] ![Usage low][usage-low]

#### [Poedit](https://poedit.net/download) - Translations made easy
![Free][licence-free-limit] ![Usage low][usage-low]

##### CLI installation
```sh
brew cask install poedit
```

#### [SwitchHosts!](https://oldj.github.io/SwitchHosts/) - Hosts management & switching
![Free][licence-free] ![Usage low][usage-low]

#### [VirtualBox](https://www.virtualbox.org/) - In case I need to debug on Windows
![Free][licence-free] ![Usage low][usage-low]

#### [Smart JSON Editor](http://www.smartjsoneditor.com/) - JSON data manipulation for Mac
![Free][licence-free-limit] ![Licence ~$10][licence-10]

Free alternative [Jayson](https://jayson.app/)

#### [Carbonize](https://www.dangercove.com/carbonize/) - Generate beautiful code snippets

#### [CodeKit](https://codekitapp.com/) - Gulp, Grunt, Pug are on a boat
![Licence ~$34][licence-30] ![Usage low][usage-low]

#### [Haskell](http://haskellformac.com/) - Haskell for Mac IDE
![Licence ~$30][licence-30] ![Usage low][usage-low]

#### [Querious](https://www.araelium.com/querious) - MySQL database management
![Free][licence-free] ![Usage low][usage-low]

### Communication

#### [Slack](https://slack.com) - Work chat
![Free][licence-free] ![Usage high][usage-high]

```sh
mas install 803453959
```

#### [Airmail]() - Email client
![Free][licence-free-limit] ![Yearly subscription][subscription-yearly] ![Backup iCloud][backup-icloud] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install 

mas install 918858936
```

### Social Media

I have a strict rule in regards to social apps on my professional Mac. I usually don't have any social / communication app that is not directly related to work (only Slack).

#### [Flume](https://flumeapp.com/) - To manage Instagram on Mac
![Free][licence-free] ![Usage low][usage-low]

#### WhatApps
![Free][licence-free] ![Usage low][usage-low]

#### Discord
![Free][licence-free] ![Usage low][usage-low]

#### Messenger
![Free][licence-free] ![Usage low][usage-low]

#### Skype
![Free][licence-free] ![Usage low][usage-low]

##### CLI installation
```sh
brew cask install skype
```

#### Telegram

##### CLI installation

```sh
mas install 747648890
```

#### [Reeder](https://reederapp.com/) - News reader
![Licence ~$13][licence-10] ![Usage high][usage-high]

##### CLI installation
```sh
mas install 880001334
```

#### [DEVONagent Pro](https://www.devontechnologies.com/apps/devonagent) - Search the web

#### [DEVONthink](https://www.devontechnologies.com/apps/devonthink) - To collect, organize and edit all my documents
![Licence ~200](https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=~$200&color=orange) ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install devonthink-pro
```

### Writing
#### [Notion](https://www.notion.so) - 
![Yearly subscription][subscription-yearly] ![Proprietary backup][backup-proprietary] ![High usage][usage-high]

evernote

##### CLI installation
```sh
brew cask install notion
```

#### [MWeb](https://www.mweb.im/) - 
![Licence ~$20][licence-20] ![Backup iCloud][backup-icloud] ![Usage high][usage-high]

#### [MindNode](https://mindnode.com) - Interactive Mind Mapping
![Licence ~$30][licence-30] ![Backup iCloud][backup-icloud] ![High medium][usage-medium]

##### CLI installation
```sh
brew cask install mindnode-pro
```

#### [Scrivener](https://www.literatureandlatte.com/scrivener/overview) - 
![Usage low][usage-low]

#### [Scapple](https://www.literatureandlatte.com/scapple/overview) - 
![Usage medium][usage-medium]

#### [Apple Keynote](https://www.apple.com/keynote/)


### Reading

Books
Calibre


#### [VLC](https://www.videolan.org/vlc/index.html) - Video
![Free][licence-free] ![Usage high][usage-high]

### Design

#### [Eagle](https://en.eagle.cool/) - Organize my design library
![Yearly subscription][subscription-yearly] ![Usage high][usage-high] ![Backup Dropbox][backup-dropbox]

#### [Rightfont 5](https://rightfontapp.com/) - Font manager
![Licence ~$35][licence-30] ![Usage medium][usage-medium] ![Backup Dropbox][backup-dropbox]

#### [IconJar](https://geticonjar.com/) - Best icon manager
![Usage low][usage-low] ![Backup Dropbox][backup-dropbox]

#### Adobe Creative Cloud
![Monthly subscription][subscription-montly] ![Proprietary backup][backup-proprietary] ![Usage high][usage-high]

##### CLI installation
```sh
brew cask install adobe-creative-cloud
```

#### Figma 
![Usage low][usage-low] ![Usage medium][usage-medium]

##### CLI installation
```sh
brew cask install figma
```

#### Sketch
![Usage medium][usage-medium] ![Backup Dropbox][backup-dropbox]

##### CLI installation
```sh
brew cask install sketch
```

Sketchpacks

#### Sip
![Yearly subscription][subscription-yearly] ![Usage medium][usage-medium]

##### CLI installation
```sh
brew cask install sip
```

#### ImageOptim

##### CLI installation
```sh
brew cask install imageoptim
```







### Audio / Video production

#### Loopback
#### Audio Hijack
#### Ecamm Live

#### [Screenflow](https://www.telestream.net/controls/screenflow/download-screenflow.htm) - Screen recording
![Usage low][usage-low] ![Backup Dropbox][backup-dropbox]

Screenflow doesn't recommend to store files on Dropbox

#### Streamlabs OBS
#### Power Prompter
#### Twitch


### Others

KeyKey
Type Fu
Typesy
MacFamilyTree 9
Team Viewer

#### Airy

##### CLI installation
```sh
brew cask install airy
```

KeyCastr

#### GPG Keychain
#### Hue Sync
![Usage low][usage-low]



#### [balenaEtcher]() - RaspberryPi microSim flasher
![Usage low][usage-low]

##### CLI installation

```sh
brew cask install bartender
```


## Preference Panes

- [GPG Suite](https://gpgtools.org/) - Encrypt, decrypt, sign and verify files or messages.
  - I use this also for signing my commits.

Hazel

## Web Applications




## Inspiration

Heavily inspired by the works from:

- https://github.com/nikitavoloboev/my-mac-os
- https://github.com/donnemartin/dev-setup

## Licence

MIT

[licence-free]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=FREE&color=green
[licence-free-limit]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=FREE%20with%20limits&color=green
[licence-10]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=~$10&color=orange
[licence-20]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=~$20&color=orange
[licence-30]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=~$30&color=orange
[licence-50]: https://img.shields.io/static/v1?style=flat-square&label=LICENCE&message=~$50&color=orange

[subscription-montly]: https://img.shields.io/static/v1?style=flat-square&label=SUBSCRIPTION&message=montly&color=red
[subscription-yearly]: https://img.shields.io/static/v1?style=flat-square&label=SUBSCRIPTION&message=yearly&color=red

[backup-icloud]: https://img.shields.io/static/v1?style=flat-square&label=Backup&message=iCloud&color=1abc9c
[backup-dropbox]: https://img.shields.io/static/v1?style=flat-square&label=Backup&message=Dropbox&color=1abc9c
[backup-proprietary]: https://img.shields.io/static/v1?style=flat-square&label=Backup&message=Proprietary&color=1abc9c

[since-2016]: https://img.shields.io/static/v1?style=flat-square&label=Using%20since&message=2016&color=1f425f
[since-2017]: https://img.shields.io/static/v1?style=flat-square&label=Using%20since&message=2017&color=1f425f
[since-2018]: https://img.shields.io/static/v1?style=flat-square&label=Using%20since&message=2018&color=1f425f
[since-2019]: https://img.shields.io/static/v1?style=flat-square&label=Using%20since&message=2019&color=1f425f

[usage-high]: https://img.shields.io/static/v1?style=flat-square&label=Usage&message=high&color=yellow
[usage-medium]: https://img.shields.io/static/v1?style=flat-square&label=Usage&message=medium&color=yellow
[usage-low]: https://img.shields.io/static/v1?style=flat-square&label=Usage&message=low&color=yellow

[support]: https://img.shields.io/static/v1?style=flat-square&label=Support&message=this%20app&color=purple