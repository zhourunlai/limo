---
title: "BUIDL NODE OPERATOR"
date: 2022-09-10T11:30:03+00:00
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

## 1. Introduction
https://rocketpool.net/node-operators  


## 2. Choose local or cloud
Local: [#stakefromhome](https://twitter.com/hashtag/stakefromhome)  
  
Cloud: [ovh adv-1](https://www.ovhcloud.com/asia/bare-metal/advance/adv-1/)  

  
## 3. Install
```shell
wget https://github.com/rocket-pool/smartnode-install/releases/latest/download/rocketpool-cli-linux-amd64 -O ~/bin/rocketpool

chmod +x ~/bin/rocketpool

rocketpool service install
```
![rocketpool](/images/rocketpool.jpeg)


## 4. Choose client
[https://client-diversity.netlify.app/](https://client-diversity.netlify.app/)

| Eth1 client	| Type	| CPU Usage	| Minimum RAM Usage	| Sync Time | 
| ----------- | ----------- | ----------- | ----------- | ----------- |
| Geth	| Full	| Moderate	| 4 GB	| Moderate | 
| Besu	| Full	| Moderate	| 8 GB	| Slow | 
| Nethermind	| Full	| Moderate	| 16 GB	| Fast | 

| Eth2 client	| CPU Usage	| Minimum RAM Usage	| Sync Time
| ----------- | ----------- | ----------- | ----------- |
| Lighthouse	| Moderate	| 2 GB	| Moderate (normal sync) Instant with checkpoint sync | 
| Nimbus	| Low	| 0.75 GB	| Moderate (normal sync) Instant with checkpoint sync | 
| Prysm	| Moderate	| 2 GB	| Moderate | 
| Teku	| Moderate	| 4 GB	| Slow (normal sync) Instant with checkpoint sync | 


## 5. Register
https://rocketscan.io/node/0xA2F7508f6240e2f74003a3281aB88C7fa0FEe648  


## 6. Monitor
![rocketpool-monitor](/images/rocketpool-monitor.png)
![rocketpool-monitor-mobile](/images/rocketpool-monitor-mobile.jpeg)