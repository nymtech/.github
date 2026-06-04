![Nym](https://raw.githubusercontent.com/nymtech/Nym-brand-assets/main/Nym.png)

# Nym

**Nym is a privacy platform that provides network-level privacy against mass surveillance — protecting not just *what* you communicate, but *who* you talk to, *when*, and *how often*.**

Encryption hides content, but it leaks metadata: traffic patterns, timing, and the social graph around every connection. Nym closes that gap with a decentralized **mixnet** — a network of independently operated nodes that encrypt, reorder, and mix traffic with cover traffic to defeat the timing and traffic-analysis attacks that deanonymize ordinary VPNs and Tor.

The design and cryptography are described in the [Nym Whitepaper](https://nym.com/nym-whitepaper.pdf).

Visit us on [nym.com](https://nym.com) to learn more about how Nym is making the Internet private by default.

## How the Nym mixnet works

```
                      ┌─►mix──┐  mix     mix
                      │       │
            Entry     │       │                   Exit
client ───► Gateway ──┘  mix  │  mix  ┌─►mix ───► Gateway ───► internet
                              │       │
                              │       │
                         mix  └─►mix──┘  mix
```

Traffic enters through a gateway and crosses multiple mix nodes that batch and shuffle [Sphinx](https://github.com/nymtech/sphinx) packets before exiting to the internet — so no single node sees both the source and the destination. Anonymous **zk-nym** credentials (built on the Coconut signature scheme) let users authenticate and pay without linking identity to activity, and node operators are incentivized through the **Nyx** blockchain.

Network "noise" – cover traffic, timing delays, and packet mixing – protect your traffic even against advanced AI surveillance. 

## NymVPN — Nym's flagship app

[**NymVPN**](https://github.com/nymtech/nym-vpn-client) puts the mixnet in everyone's hands. It's an open-source, cross-platform dVPN (Android, iOS, Linux, macOS, Windows, CLI) with two routing modes: a 5-hop **Mixnet Mode** over the mixnet for metadata protection, and a 2-hop **Fast Mode** over AmneziaWG (WireGuard) for low-latency, censorship-resistant browsing. No email or account identity is required to connect.

## What's in this organization

| Repo | What it is |
|---|---|
| [`nym`](https://github.com/nymtech/nym) | The core privacy platform — `nym-node` (mix nodes & gateways), clients, SOCKS5 proxy, wallet, SDKs, and CLI. Rust. |
| [`nym-vpn-client`](https://github.com/nymtech/nym-vpn-client) | **NymVPN** — the consumer dVPN app for Android, iOS, Linux, macOS, Windows, and CLI. |
| [`sphinx`](https://github.com/nymtech/sphinx) | Rust implementation of the Sphinx packet format that powers mixnet routing. |
| [`nyxd`](https://github.com/nymtech/nyxd) | Nyx validator node — a CosmWasm/`wasmd` fork securing payments and operator rewards. |
| [`developer-tutorials`](https://github.com/nymtech/developer-tutorials) | Finished code for the Nym developer tutorials. |

## Build on Nym

Route any application's traffic through the mixnet using the Nym clients and SDKs.

- [Developer Docs](https://nym.com/docs/developers) · [Rust SDK](https://nym.com/docs/developers/rust)
- [Network Docs](https://nym.com/docs/network) · [Operators Guide](https://nym.com/docs/operators)

## Community

[![Telegram](https://img.shields.io/badge/Telegram-26A5E4.svg?style=for-the-badge&logo=Telegram&logoColor=white)](https://nym.com/go/telegram)
[![Matrix](https://img.shields.io/badge/Matrix-000000.svg?style=for-the-badge&logo=Matrix&logoColor=white)](https://nym.com/go/matrix)
[![Discord](https://img.shields.io/badge/Discord-5865F2.svg?style=for-the-badge&logo=Discord&logoColor=white)](https://nym.com/go/discord)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://nym.com/go/youtube)
[![X](https://img.shields.io/badge/X-000000.svg?style=for-the-badge&logo=X&logoColor=white)](https://nym.com/go/x)

---

©2018–2026 Nym Technologies SA · [nym.com](https://nym.com) · [contact@nymtech.net](mailto:contact@nymtech.net)
