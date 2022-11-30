# Original author: mack-a
# Original project: https://github.com/mack-a/v2ray-agent

# v2ray-agent

> [Chinese Version](https://github.com/reeceyng/v2ray-agent/blob/master/README.md)

- [Cloudflare Optimization Solution](https://github.com/reeceyng/v2ray-agent/blob/master/documents/optimize_V2Ray.md)
- [Traffic Relay](https://github.com/reeceyng/v2ray-agent/blob/master/documents/traffic_relay.md)
- [manual self-build tutorial](https://github.com/reeceyng/v2ray-agent/blob/master/documents/Cloudflare_install_manual.md)
- **Please give a ⭐ support**

* * * 

# Catalog

- [1.Script installation](#1vlesstcptlsvlesswstlsvmesstcptlsvmesswstlstrojan-camouflage site-five-in-one coexistence script)
  - [Features](#Features)
  - [Notes](#Notes)
  - [Installation Script](#installation-script)

* * * 

# 1.Eight-in-one coexistence script+ Mock Site

- [Cloudflare Getting Started Tutorial](https://github.com/reeceyng/v2ray-agent/blob/master/documents/cloudflare_init.md)

## Features
- Support [Xray-core[XTLS]](https ://github.com/XTLS/Xray-core), [v2ray-core](https://github.com/v2fly/v2ray-core)
- support VLESS/VMess/trojan protocol
- supports VLESS/Trojan prepending [VLESS XTLS -> Trojan XTLS], [Trojan XTLS -> VLESS XTLS]
- Support mutual reading of configuration files between different cores
- Trojan+TCP+xtls-rprx-direct
- Support Debian, Ubuntu, Centos systems and mainstream CPU architectures.
- Support any combination of installation, support for multi-user management, support for DNS streaming media unlock, support for adding multiple ports, [support any door to unlock Netflix](https://github.com/reeceyng/v2ray-agent/blob/master/documents/netflix/dokodemo-unblock_netflix.md)
- support to keep tls certificate after uninstall
- support for IPv6, [IPv6 note](https://github.com/reeceyng/v2ray-agent/blob/master/documents/ipv6_help.md)
- Support WARP offload, IPv6 offload
- Support BT download management, log management, domain name blacklist management, core management, camouflage site management
- [Support custom certificate installation](https://github.com/reeceyng/v2ray-agent/blob/master/documents/install_tls.md)

## Supported installation types

- VLESS+TCP+TLS
- VLESS+TCP+xtls-rprx-direct
- VLESS+gRPC+TLS [support CDN, IPv6, delay Low]
- VLESS+WS+TLS [support CDN, IPv6]
- Trojan+TCP+TLS [**recommended**]
- Trojan+gRPC+TLS [support CDN, IPv6, low latency]
- VMess+WS+TLS [support CDN, IPv6]

## Route recommendation

- CN2 GIA
- Shanghai CN2+HK
- AS9929
- AS4837
- Unicom Japan Softbank
- Unicom+ Taiwan TFN
- China Unicom+NTT
- Guangzhou Mobile/Zhushift+HKIX/CMI/NTT
- Guangzhou Mobile/CN2+Cloudflare+ Global
- Guangzhou Mobile/CN2/South Union+Hong Kong AZ+Global
- Transit+cloudflare+Landing Machine【Kela Global】

## Precautions

- **Modify Cloudflare->SSL/TLS->Overview->Full**
- **Cloudflare ---> Clouds parsed by A record must be gray [if not gray, it will affect the automatic renewal certificate of scheduled tasks]**
- **If you use CDN and direct connection at the same time, turn off Yunduo + self-selected IP, refer to the above [Cloudflare optimization plan](https://github.com/reeceyng/v2ray-agent/blob/master/documents/optimize_V2Ray.md)**
- **Use the pure system to install, if you have installed it with other scripts and you cannot modify the error yourself, please reinstall the system and try to install again**
- wget: command not found [**Here you need to do it manually Install wget**]
  , if you have not used Linux, [click to view](https://github.com/reeceyng/v2ray-agent/tree/master/documents/install_tools.md) installation tutorial
- does not support non- root account
- **If you find Nginx-related problems, please uninstall the self-compiled nginx or reinstall the system**
- **In order to save time, please bring detailed screenshots or follow the template specifications for feedback, no screenshots or issues that do not follow the specifications Will be closed directly**
- **Not recommended for GCP users**
- **Oracle Cloud has an additional firewall that needs to be set manually**
- **Centos and lower versions of the system are not recommended, if the Centos installation fails, please switch to Debian10 and try again, the script no longer supports Centos6 , Ubuntu 16.x**
- **[If you don't understand the usage, please check the script usage guide first](https://github.com/reeceyng/v2ray-agent/blob/master/documents/how_to_use.md)**
- ** Oracle Cloud only supports Ubuntu**
- **If you use gRPC to forward through cloudflare, you need to allow gRPC in cloudflare settings, path: cloudflare Network->gRPC**
- **gRPC is currently in beta and may not work for the client you use Compatible, if you can't use it, please ignore **
- ** The problem that the lower version script cannot be started when upgrading the higher version, [please click this link to view the solution](https://github.com/reeceyng/v2ray-agent/blob/master/documents/how_to_use.md#4%E4%BD%8E%E7%89%88%E6%9C%AC%E5%8D%87%E7%BA%A7%E9%AB%98%E7%89%88%E6%9C%AC%E5%90%8E%E6%97%A0%E6%B3%95%E5%90%AF%E5%8A%A8%E6%A0%B8%E5%BF%83)**

## Installation script

- supports shortcut startup, after installation, enter [**vasma**] in the shell You can open the script, the script execution path [**/etc/v2ray-agent/install.sh**]

- Latest Version [recommended]

``` 
wget -P/root -N --no-check-certificate "https://raw.githubusercontent.com/reeceyng/v2ray-agent/master/shell/install_en.sh" && mv /root/install_en.sh /root/install.sh && chmod 700 /root/install.sh &&/root/install.sh
``` 


# example image

<img src="https://raw.githubusercontent.com/reeceyng/v2ray-agent/master/fodder/install/install.jpg" width=700>

# licence

[AGPL-3.0](https://github.com/reeceyng/v2ray-agent/blob/master/LICENSE)

## Stargazers over time

[![Stargazers over time](https://starchart.cc/reeceyng/v2ray-agent.svg)](https://starchart.cc/reeceyng/v2ray-agent)
