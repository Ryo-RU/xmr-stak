[<img src="doc/_img/main-banner.png">](https://github.com/fireice-uk/xmr-stak/releases/latest)

## Contents
|  |  |
| ---  | ---  |
| 1. [Introduction](#introduction) | 5. [Start mining](#start-mining) |
| 2. [Features](#features) | 6. [Guides and feedback](#additional-guides-and-feedback) |
| 3. [Supported coins and algorithms](#supported-coins-and-algorithms) | 7. [Developer Donation](#default-developer-donation) |
| 4. [Get miner](#get-miner) | 8. [Developer PGP Key's](/doc/pgp_keys.md) |


## Introduction
XMR-Stak is a universal open source stratum pool miner. This miner supports CPUs, AMD and NVIDIA GPUs and can be used for mining various crypto currencies: Ryo, Monero, Turtlecoin, Graft, Bittube, Aeon and many more Cryptonight coins.


## Features
- Supports all common backends (CPU/x86, AMD/NVIDIA GPU).
- Supports all common OS (Linux, Windows and macOS).
- Supports 15 cryptonight-variant mining algorithms + Cryptonight-GPU.
- Easy to use and flexible in setup:
  - Guided start with easy/advanced setup option (no need to edit a config file for the first start).
  - Auto-configuration and config file creation for each backend.
  - Optional built-in auto-tune feature (helps a user to check intensity values in range).
- Benchmark mode.
- TLS support.
- [JSON API for monitoring](/doc/usage.md#HTML-and-JSON-API-report-configuration)
- [Web monitoring and statistics (html reports)](/doc/usage.md#HTML-and-JSON-API-report-configuration)
[<img src="doc/_img/html_reports.png">](/doc/usage.md#HTML-and-JSON-API-report-configuration)

## Supported coins and algorithms
Following coins can be mined using this miner:

|  |  |
| ---  | ---  |
| [Aeon](http://www.aeon.cash) | [Plenteum](https://www.plenteum.com/) |
| [BitTube](https://coin.bit.tube/) | [QRL](https://theqrl.org) |
| [Conceal](https://conceal.network) | **[Ryo](https://ryo-currency.com) - Upcoming xmr-stak-gui is sponsored by Ryo Currency** |
| [Graft](https://www.graft.network) | [Torque](https://torque.cash/) |
| [Haven](https://havenprotocol.com) | [TurtleCoin](https://turtlecoin.lol) |
| [Lethean](https://lethean.io) | [X-CASH](https://x-network.io/) |
| [Masari](https://getmasari.org) | [Zelerius](https://zelerius.org/) |
| [Monero](https://getmonero.org) |  |

**[Ryo Currency](https://ryo-currency.com)** - is a way for us to implement the ideas that we were unable to in
Monero. See [here](https://github.com/fireice-uk/cryptonote-speedup-demo/) for details.

If your preferred coin is not listed, you can choose one of the following mining algorithms:

| 256 Kib scratchpad memory |  |
| ---  | ---  |
| Cryptonight_turtle |  |

| 1 MiB scratchpad memory |  |
| ---  | ---  |
| cryptonight_lite | cryptonight_lite_v7 |
| cryptonight_lite_v7_xor (algorithm used by ipbc) |  |

| 2MiB scratchpad memory |  |
| ---  | ---  |
| cryptonight | cryptonight_v7 |
| cryptonight_gpu (for Ryo's 14th of Feb fork) | cryptonight_v7_stellite |   
| cryptonight_conceal | cryptonight_v8 |   
| cryptonight_r  | cryptonight_v8_half (used by masari and torque) |   
| cryptonight_masari (used in 2018) | cryptonight_v8_double (used by X-CASH)  |   
|  | cryptonight_v8_zelerius |   
|  | cryptonight_v8_reversewaltz (used by graft) |   
   
| 4 MiB scratchpad memory |  |
| ---  | ---  |
| cryptonight_haven | cryptonight_heavy |



Please note, this list is not complete and is not an endorsement.


## Get Miner
Please note that code is developed on the [dev branch](https://github.com/fireice-uk/xmr-stak/commits/dev), if you want to check out the latest updates, before they are merged on main branch, please refer there. Master branch will always point to a version that we consider stable, so you can download the code by simply typing `git clone https://github.com/fireice-uk/xmr-stak.git`  

Also you can find the latest releases and precompiled binaries on GitHub under [releases](https://github.com/fireice-uk/xmr-stak/releases/latest) section.

If you want to compile the miner from source files, navigate to ["how to compile"](/doc/compile/compile.md) section of docs or [xmr-stak forum](https://www.reddit.com/r/XmrStak/wiki/guides/startup) where you will find the latest step-by-step instructions.


## Start Mining
Miner has 2 ways of initial configuring: simple and advanced. The simple method will prompt user with minimum information. Required answers are y , (or yes), n , (or no):

#### Simple setup:
* `Use simple setup method?` y    
* `Please enter the currency that you want to mine:` Enter currency or mining algorithm  
* `Enter pool address (pool address:port):` Enter pool connection address:port  
* `Username (wallet address or pool login):` Enter wallet address
* `Password (mostly empty or x):` press Enter  
* `Does this pool port support TLS/SSL? Use no if unknown. (y/N):` press y or n  

#### Advanced setup:
* `Use simple setup method?` n  
* `Do you want to use the HTTP interface? Unlike the screen display, browser interface is not affected by the GPU lag. If you don't want to use it, please enter 0, otherwise enter port number that the miner should listen on` 5656
* `Please enter the currency that you want to mine:` Enter currency or mining algorithm
* `Enter pool address (pool address:port):` Enter pool connection address:port 
* `Username (wallet address or pool login):` Enter wallet address
* `Password (mostly empty or x):` press Enter
* `Rig identifier for pool-side statistics (needs pool support). Can be empty:` Enter rig name or press Enter
* `Does this pool port support TLS/SSL? Use no if unknown. (y/N)` Enter y or n
* `Do you want to use nicehash on this pool? (y/N)` n
* `Do you want to use multiple pools? (y/N)` Enter y if you want to se up backup pool or n

## Additional Guides and Feedback
[<img src="doc/_img/stak-yt-cover.jpg">](https://www.youtube.com/playlist?list=PLAhUkom29iGMFoN8pk91JA-oqvxlmJ5H8)
###### Video by Crypto Sewer

To improve our support we created [Xmr-Stak forum](https://www.reddit.com/r/XmrStak). Check it out if you have a problem, or you are looking for most up to date config for your card and [guides](https://www.reddit.com/r/XmrStak/wiki/index).
* [Usage](/doc/usage.md)
* [How to compile](/doc/compile/compile.md)
* [Fine tuning](/doc/tuning.md)
* [FAQ](/doc/FAQ.md)
* [Troubleshooting](/doc/troubleshooting.md) (Fixing common problems)


## Default Developer Donation
By default, the miner will donate 2% of the hashpower (2 minutes in 100 minutes) to my pool. If you want to change that, edit [donate-level.hpp](xmrstak/donate-level.hpp) before you build the binaries.

If you want to donate directly to support further development, here is my wallet

fireice-uk:
```
4581HhZkQHgZrZjKeCfCJxZff9E3xCgHGF25zABZz7oR71TnbbgiS7sK9jveE6Dx6uMs2LwszDuvQJgRZQotdpHt1fTdDhk
```

psychocrypt:
```
45tcqnJMgd3VqeTznNotiNj4G9PQoK67TGRiHyj6EYSZ31NUbAfs9XdiU5squmZb717iHJLxZv3KfEw8jCYGL5wa19yrVCn
```
