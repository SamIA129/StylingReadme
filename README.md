# Pingora
![Pingora](https://habrastorage.org/r/w1560/webt/pd/xp/vm/pdxpvmwi52mvghrgnypigfgjyki.png)
## What is Pingora
Pingola is a framework to [built fast, reliable and programmable networked system](https://blog.cloudflare.com/pingora-open-source).<br>
Pingola is battle tested as it has been serving more than 40 million Internet requests per second for [more than a few years](https://blog.cloudflare.com/how-we-built-pingora-the-proxy-that-connects-cloudflare-to-the-internet).

## Feature highlights
+ Asung Rust: fast and reliable
+ HTTP 1/2 end to end proxy
+ TLS over OpenSSL or BoringSSL
+ gRPC and websocket proxying
+ Graceful reload
+ Customizable load balancing and failover strategies
+ Support for a variety of observability tools

## Reason to use Pingora
+ Security is your top priority: Pingora is a more memory safe alternative for services that are written in C/C++
+ Your service is <b>performance-sensitive</b>: Pingora is fast and efficient
+ Your service requires extensive <b>customization</b>: The APIs Pingora proxy framework provides are highly programmable

# Getting started
See our [quick starting guide](https://github.com/cloudflare/pingora/blob/main/docs/quick_start.md) to see how easy it is to build a load balancer.
<br><br>
Our [user guide](https://github.com/cloudflare/pingora/blob/main/docs/user_guide/index.md) covers more topics such as how to configure and run Pingora servers, as well as how to build custom HTTP servers and proxy logic on top of Pingora's framework.
<br><br>
API docs are also available for all the crates.

# Notable crates in this workspace
+ Pingora: the "public facing" crate to build networked systems and proxies
+ Pingora-core: this crate defines the protocols, functionalities and basic traits
+ Pingora-proxy: the logic and APIs to build HTTP proxies
+ Pingora-error: the common error type used across Pingora crates
+ Pingora-http: the HTTP header definitions and APIs
+ Pingora-openssl & pingora-boringssl: SSL related extensions and APIs
+ Pingora-ketama: the [Ketama](https://github.com/RJ/ketama) consistent algorithm
+ Pingora-limits: efficient counting algorithms
+ Pingora-load-balancing: load balancing algorithm extensions for pingora-proxy
+ Pingora-memory-cache: Async in-memory caching with cache lock to prevent cache stampede
+ Pingora-timeout: A more efficient async timer system
+ TinyUfo: The caching algorithm behind pingora-memory-cache

# System requirements
## System
Linux is our tier 1 environment and main focus.
<br><br>
We will try our best for most code to compile for Unix environments. This is for developers and users to have an easier time developing with Pingora in Unix-like environments like macOS (though some features might be missing)
<br><br>
Both x86_64 and aarch64 architectures will be supported.

## Rust version
Pingora keeps a rolling MSRV (minimum supported Rust version) policy of 6 months. This means we will accept PRs that upgrade the MSRV as long as the new Rust version used is at least 6 months old.

Our current MSRV is 1.72.

# Contributing
Please see our [contribution guidelines](https://github.com/cloudflare/pingora/blob/main/.github/CONTRIBUTING.md).

# License
This project is Licensed under [Apache License, Version 2.0](https://github.com/cloudflare/pingora/blob/main/LICENSE)

> [!WARNING]
> Текст переписан, так как у создателя репозитория нет фантазии
