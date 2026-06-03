<!-- ========================================================================= -->
<!--                        YTDLBOT — README                            -->
<!--       Cyberpunk Premium Theme  |  Animated SVGs  |  Live Badges          -->
<!-- ========================================================================= -->

<div align="center">

<!-- ============================== BANNER ============================== -->

<img src="https://capsule-render.vercel.app/api?type=color_wave&color=0:000000,30:002E1A,70:001A0D,100:000000&height=180&section=header&text=ytdlbot&fontSize=48&fontColor=00FF88&fontAlignY=38&animation=fadeIn" width="100%"/>

<!-- ============================== TYPING SVG ============================== -->

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Source%20Code%20Pro&weight=500&size=22&duration=3500&pause=800&color=00FF88&center=true&vCenter=true&multiline=true&repeat=true&random=false&width=700&height=80&lines=%3E%20Welcome%20to%20ytdlbot%20%F0%9F%9A%80;%3E%20Built%20using%20Code%20%7C%20Optimized%20%26%20Secure;%3E%20Download%20videos%20from%20Youtube%20and%20other%20p...)](https://github.com/VarshuAi/ytdlbot)

<br/>

![Version](https://img.shields.io/badge/Version-1.0-00FF88?style=for-the-badge&logo=github&logoColor=black)
![Language](https://img.shields.io/badge/Code-Tech-00CC66?style=for-the-badge&logo=code&logoColor=black)
![Status](https://img.shields.io/badge/Status-Active-14354C?style=for-the-badge&logo=git&logoColor=white)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,30:002E1A,70:001A0D,100:000000&height=60&section=header&text=&fontSize=0" width="100%"/>

</div>

<!-- ============================== ABOUT ============================== -->

<h2>
<img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="30">
<samp>&nbsp;ABOUT</samp>
</h2>

```yaml
name: ytdlbot
version: 1.0
type: Repository
author: VarshuAi
description: >
  Download videos from Youtube and other platforms through a Telegram Bot
primary_tech: Code
```

<!-- ============================== CENTRAL GRAPHIC ============================== -->

<div align="center">
<br>
<div align="center"><img src="https://media.giphy.com/media/3o85xr9ibKf1AlikhO/giphy.gif" alt="Cyberpunk Grid Animation" width="100%"/></div>
<br>
</div>

<!-- ============================== FEATURES ============================== -->

<h2>
<img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="28">
<samp>&nbsp;FEATURES</samp>
</h2>

### 6.1 Setup flower db

Get pod running ytdl master:

```shell
kubectl get pods --namespace ytdl
```

Name should be ytdl-xxxxxxxx

Access to pod

```shell
kubectl --namespace=ytdl exec --stdin --tty ytdl-xxx -- sh
```

(replace ytdl-xxx by your pod name)

Go to ytdl-pvc mounted folder

```shel
cd /var/lib/vnstat/
```

Create flower database file

```shell
{} ~ python3
Python 3.9.9 (main, Nov 21 2021, 03:22:47)
[Clang 12.0.0 (clang-1200.0.32.29)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import dbm;dbm.open("flower","n");exit()
```

### 6.2 Config Flower Ingress

This step need config ingress from line 51 of file 06.flower.yml with your ingress service. Need for access from
internet.
YML file should be adjusted depending on your load balancing, ingress and network system

For active SSL

```yml
cert-manager.io/cluster-issuer: letsencrypt-prod
```

Replace nginx by your ingress service

```yml
ingressClassName: nginx
```

Add your domain, example

```yml
tls:
  - hosts:
      - flower.benny.com
    secretName: flower-tls
  rules:
    - host: flower.benny.com
```

### 6.3 Apply Flower deloyment

```shell
kubectl apply -f 06.flower.yml
```

# Command

```
start - Let's start
about - What's this bot?
ping - Bot running status
help - Help
ytdl - Download video in group
vip - Join VIP
settings - Set your preference
direct - Download file directly
sub - Subscribe to YouTube Channel
unsub - Unsubscribe from YouTube Channel
sub_count - Check subscription status, owner only.
uncache - Delete cache for this link, owner only.
purge - Delete all tasks , owner only.
topup - Top up quota
tgvip - Using Telegram payment to pay for VIP
```

# Test data

<!-- ============================== COMMANDS ============================== -->

<h2>
<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="28">
<samp>&nbsp;COMMANDS & USAGE</samp>
</h2>

```shell
kubectl apply -f 05.ytdl-worker.yml
```

<!-- ============================== TECH STACK ============================== -->

<h2>
<img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="28">
<samp>&nbsp;TECH STACK</samp>
</h2>

<div align="center">

#### `>> SYSTEM INVENTORY`
![Code](https://img.shields.io/badge/Code-Primary_Language-00FF88?style=for-the-badge&logoColor=black)
![Git](https://img.shields.io/badge/Git-VCS-00CC66?style=for-the-badge&logo=git&logoColor=white)

</div>

<!-- ============================== SETUP ============================== -->

<h2>
<img src="https://media.giphy.com/media/LnQjpWaON8nhr21vNW/giphy.gif" width="28">
<samp>&nbsp;SETUP</samp>
</h2>

```bash
# 1. Clone repository remote
git clone https://github.com/VarshuAi/ytdlbot.git
cd ytdlbot

# 2. Check technical prerequsites
# Ensure runtime matches requirements (Code)
```

<!-- ============================== STRUCTURE ============================== -->

<h2>
<samp>&nbsp;📁 STRUCTURE</samp>
</h2>

```
ytdlbot/
├── src/             # Source code entrypoints
├── docs/            # Project documentation files
├── README.md        # Interactive readme sheet
└── LICENSE          # Permission details
```

<!-- ============================== FOOTER ============================== -->

<div align="center">

<br/>

<img src="https://capsule-render.vercel.app/api?type=color_wave&color=0:000000,30:002E1A,70:001A0D,100:000000&height=80&section=footer&text=&fontSize=0" width="100%"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Source%20Code%20Pro&size=14&duration=4000&pause=1000&color=00FF88&center=true&vCenter=true&width=500&lines=Made+with+%E2%9D%A4%EF%B8%8F+by+VarshuAi;Build+Fast.+Ship+Secure.+Scale+Infinite.)](https://github.com/VarshuAi)

<br/>

[![GitHub](https://img.shields.io/badge/VarshuAi-Profile-00FF88?style=for-the-badge&logo=github&logoColor=black)](https://github.com/VarshuAi)
[![Repo](https://img.shields.io/badge/ytdlbot-Repo-00CC66?style=for-the-badge&logo=github&logoColor=black)](https://github.com/VarshuAi/ytdlbot)

<br/>

</div>
