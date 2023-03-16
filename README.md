# v2ray-agent

> [Thanks for non-commercial open source development authorization by JetBrains](https://www.jetbrains.com/?from=v2ray-agent)

- [Cloudflare Optimization Solutions](https://github.com/DhimasArbi/v2ray-agent/blob/master/documents/optimize_V2Ray.md)
- [Traffic Transit Tutorial](https://github.com/DhimasArbi/v2ray-agent/blob/master/documents/traffic_relay.md)
- [SSH Getting Started Tutorial](https://www.v2ray-agent.com/2020-12-16-ssh%E5%85%A5%E9%97%A8%E6%95%99%E7%A8%8B)
- [TG Group](https://t.me/technologyshare)、[TG Channel](https://t.me/joinchat/VuYxsKnlIQp3VRw-)、[Blog](https://www.v2ray-agent.com/)
- Welcome Pull request

---

# Catalog

- [1.Installation Script](#1vlesstcptlsvlesswstlsvmesstcptlsvmesswstlstrojan-伪装博客-五合一共存脚本)
  - [Characteristics](#characteristics)
  - [architecture](#architecture)
  - [Line recommendation](#line-recommendationchina)
  - [Combination recommendation](#combination-recommendation)
  - [Cautions](#cautions)
  - [Usage](#usage)

---

# 1.Seven-in-One Coexistence Script+Camouflage site

- [Cloudflare Introductory tutorial](https://github.com/DhimasArbi/v2ray-agent/blob/master/documents/cloudflare_init.md)

## Characteristics

- Support [Xray-core[XTLS]](https://github.com/XTLS/Xray-core)、v2ray-core
- Support VLESS/Trojan prepending [VLESS XTLS -> Trojan XTLS], [Trojan XTLS -> VLESS XTLS]
- Support mutual reading of configuration files between different cores
- Support VLESS/VMess/trojan protocol
- Support Debian、Ubuntu、Centos,Support mainstream cpu architecture。
- Support any combination of installation, support for multi-user management, support for DNS streaming media unlock, support for adding multiple ports, support for any door to unlock Netflix
- Support to keep tls certificate after uninstall
- Support IPv6，IPv6 precautions
- Support WARP offload, IPv6 offload
- Support BT download management, log management, domain name blacklist management, core management, disguised site management
- Support custom certificate installation

## Architecture

- VLESS+TCP+TLS
- VLESS+TCP+xtls-rprx-direct【**Recommended**】
- VLESS+WS+TLS【Support CDN、IPv6】
- VLESS+gRPC+TLS【Support CDN、IPv6】
- VMess+WS+TLS【Support CDN、IPv6】
- Trojan+TCP+TLS【**Recommended**】
- Trojan+TCP+xtls-rprx-direct【**Recommended**】
- Trojan+gRPC+TLS【Support CDN、IPv6】

## Line recommendation

- IDK, Try Yourself

## Combination recommendation

- cloudflare->VLESS+gRPC+TLS/Trojan+gRPC+TLS/Trojan+TCP+XTLS/VLESS+WS+TLS

## Cautions

- Modify Cloudflare->SSL/TLS->Overview->Full
- Cloudflare ---> A record resolution of clouds must be gray
- **If you use CDN and direct connection at the same time, turn off Cloudflare + self-selected IP, refer to the Cloudflare optimization solution above for self-selected IP**
- **Use the pure system installation, if you have installed using other scripts, please re-build the system and then install**
- wget: command not found [**Here you need to manually install the wget yourself**]
  ，If you have not used Linux，[Click to view](https://github.com/DhimasArbi/v2ray-agent/tree/master/documents/install_tools.md)Installation Tutorial
- Non-root accounts are not supported
- **The version number upgrade in the middle means that it may not be compatible with the previously installed content, so please upgrade carefully if you are not chasing new users or must upgrade the
  version. ** For example, 2.2.\*, not compatible with 2.1.\*
- **If you find Nginx-related problems, please uninstall the self-compiled nginx or re-build the system**
- **In order to save time, feedback please bring detailed screenshots or in accordance with the template specifications, no screenshots or not in accordance with the specifications of the issue will
  be directly closed**
- **Not recommended for GCP users**
- **Centos and lower versions are not recommended, Centos6 is no longer supported after 2.3.x**

## Usage

- Support shortcut start, after installation, shell input [**menu**] to open the script, script execution path [**/etc/v2ray-agent/install.sh**]

- Latest Version

```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/DhimasArbi/v2ray-agent/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```

# License

[AGPL-3.0](https://github.com/DhimasArbi/v2ray-agent/blob/master/LICENSE)

## Stargazers over time

[![Stargazers over time](https://starchart.cc/DhimasArbi/v2ray-agent.svg)](https://starchart.cc/DhimasArbi/v2ray-agent)
