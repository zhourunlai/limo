---
title: "BUIDL BTC NODE OPERATOR"
date: 2023-03-02T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["crypto"]
# author: "xiaorun"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: ""
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
---

## 1. bitcoin core

### 1.1 download
```shell
wget https://bitcoin.org/bin/bitcoin-core-22.0/bitcoin-22.0-x86_64-linux-gnu.tar.gz
```

### 1.2 edit config
```shell
vim bitcoin.conf

# Specify data directory
datadir=/home/ubuntu/.bitcoin/data

# Location of the auth cookie
rpccookiefile=/home/ubuntu/.bitcoin/data/.cookie

# Run in the background as a daemon and accept commands
daemon=1

# Maintain a full transaction index, used by the getrawtransaction rpc
txindex=1

# Accept public REST requests
rest=1

# Accept command line and JSON-RPC commands
server=1
```

### 1.3 start server
```shell
./bin/bitcoind --conf=/home/ubuntu/bitcoin/bitcoin.conf --daemon
```

### 1.4 wait to sync block(～500G)
```shell
tail -f /home/ubuntu/.bitcoin/data/debug.log

2023-03-02T03:17:27Z UpdateTip: new best=0000000000000000000567e5374d59bed7ab18f65856599f4cef924e3fc2e923 height=778914 version=0x2ae44000 log2_work=94.033371 tx=810050282 date='2023-03-02T03:17:12Z' progress=1.000000 cache=68.8MiB(500391txo)
```

![bitcoin](/images/bitcoin-log.jpg)

### 1.5 usage
```shell
./bin/bitcoin-cli --rpccookiefile=/home/ubuntu/.bitcoin/data/.cookie getblockchaininfo
```

![bitcoin](/images/bitcoin-cli.jpg)


## 2. ordinals

### 2.1 download
```shell
wget https://github.com/casey/ord/releases/download/0.5.1/ord-0.5.1-x86_64-unknown-linux-gnu.tar.gz
```

### 2.2 usage
```shell
./ord --cookie-file /home/ubuntu/.bitcoin/data/.cookie -h
****
./ord --cookie-file /home/ubuntu/.bitcoin/data/.cookie wallet restore <MNEMONIC>
```

![ordinals](/images/ord-cli.jpg)

![ordinals](/images/ord-sub.jpg)

### 2.3 inscribe
```shell
./ord wallet inscribe <FILE> --fee-rate <FEE_RATE>
```
