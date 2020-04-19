# My Mac OS setup and workflow


## My Hardware

Computer: 13" Late 2017 Macbook Pro with Touch bar.

Monitor: [LG 34UM69G-B 34" 21:9 UltraWide](https://www.amazon.ca/gp/product/B06XFXX5JH/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

Keyboards:
    - At Work: [Pock3R](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=3631) black with blue leds
    - At Home: [Ducky One 2 RGB TKL](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=4284)

Mouses:
    - 2 [Logitech MX Master 2S](https://www.amazon.ca/dp/B071YZJ1G1/ref=cm_sw_em_r_mt_dp_U_92mNEbX6PD4H0)

Accessories:
    - [Elgato Stream Deck](https://www.amazon.ca/dp/B06XKNZT1P/ref=cm_sw_em_r_mt_dp_U_64mNEbDTVAA81)
    - [Elgato Green Screen](https://www.amazon.ca/dp/B0743Z892W/ref=cm_sw_em_r_mt_dp_U_n-mNEbNJ37DDK)
    - [Focusrite Scarlett-2i2 Gen2](https://www.amazon.ca/dp/B005OZE9SA/ref=cm_sw_em_r_mt_dp_U_v7mNEb9RZNDFG)
    - [DBX 286s Microphone Pre-amp Processor](https://www.amazon.ca/dp/B004NDFRVC/ref=cm_sw_em_r_mt_dp_U_V7mNEbTJ0E20E)
    - Rode Procaster

## Setup shell

- [ ] Install [homebrew](https://brew.sh)

```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- [ ] Install [Caskfile](Caskfile)

```bash
brew install caskroom/cask/brew-cask
```

- [ ] Install [ZSH](#ZSH)

```bash
brew install zsh
```

Add this to my `./zshrc`

```
export HOMEBREW_CASK_OPTS="--appdir=/Applications"
```

- [ ] Install Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Check if Oh My Zsh was correctly installed

```bash
zsh --version
```

## Applications

### Dropbox

- [ ] Download Dropbox
- [ ] Select `Apps` and `Screenshots` folders to sync

## Inspiration

Heavily inspired by the works from:

- https://github.com/nikitavoloboev/my-mac-os
- https://github.com/donnemartin/dev-setup