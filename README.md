![](https://github.com/cossacklabs/themis/wiki/images/logo.png)

[![Join the chat at https://gitter.im/cossacklabs/themis](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cossacklabs/themis?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Circle CI](https://circleci.com/gh/cossacklabs/themis/tree/master.svg?style=shield)](https://circleci.com/gh/cossacklabs/themis)

Themis is open-source high-level cryptographic services library for mobile and server platforms, providing secure messaging and secure data storage. Current stable release is [0.9.2](https://github.com/cossacklabs/themis/releases/tag/0.9.2), dated 6th of November.

Themis works in most operating systems (see [Availability](https://github.com/cossacklabs/themis#availability)), and is available for [Swift (iOS, OX)](https://github.com/cossacklabs/themis/wiki/Swift-Howto), [Objective-C (iOS, OX)](https://github.com/cossacklabs/themis/wiki/Objective-C-Howto), [Java / Android](https://github.com/cossacklabs/themis/wiki/Android-Howto),  [Ruby](https://github.com/cossacklabs/themis/wiki/Ruby-Howto),  [Python](https://github.com/cossacklabs/themis/wiki/Python-Howto), 
[PHP](https://github.com/cossacklabs/themis/wiki/PHP-Howto), 
[C++](https://github.com/cossacklabs/themis/wiki/CPP-Howto), 
[Javascript (NodeJS)](https://github.com/cossacklabs/themis/wiki/NodeJS-Howto),
[Google Chrome](https://github.com/cossacklabs/webthemis). 

Themis provides three important cryptographic services:
* [Secure Message](https://github.com/cossacklabs/themis/wiki/Secure-Message-cryptosystem): a simple encrypted messaging solution  for widest scope of applications. ECC + ECDSA / RSA + PSS + PKCS#7.
* [Secure Session](https://github.com/cossacklabs/themis/wiki/Secure-Session-cryptosystem): session-oriented, forward secrecy messaging solution with better security guarantees, but more demanding infrastructure. ECDH key agreement, ECC & AES encryption.
* [Secure Cell](https://github.com/cossacklabs/themis/wiki/Secure-Cell-cryptosystem): a multi-mode cryptographic container, suitable for storing anything from encrypted files to database records and format-preserved strings. Secure Cell is built around AES in GCM (Token and Seal modes) and CTR (Context imprint mode).

Themis was designed to provide complicated cryptosystems in easy-to-use infrastructure, suitable for modern rapid development. Themis is based on best modern practices in implementing complicated security systems based on strongest available cryptographic algorithms in their safest forms. It is available for modern mobile and server languages (see below).

Themis is open source, Apache 2 Licensed.

# Quickstart

1. Fetch the repository: git clone https://github.com/cossacklabs/themis.git
2. Have OpenSSL/LibreSSL + OpenSSL/LibreSSL Dev package (libssl-dev) installed at typical paths: `/usr/lib`, `/usr/include`. 
3. Have typical GCC/clang environment installed
4. Type 'make install' and you're done (most of the cases)
5. Dive into [our wiki](https://github.com/cossacklabs/themis/wiki) for the docs of language of your choice, take a look at docs/examples for examples. 

It is really advisable to [go the long way and read the docs](https://github.com/cossacklabs/themis/wiki/3.1-Building-and-installing), but god blesses the brave.

# Languages

Themis is available for the following languages: 

- Swift (iOS, OSX) [documentation](https://github.com/cossacklabs/themis/wiki/Swift-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/swift)
- Objective-C (iOS, OSX) [documentation](https://github.com/cossacklabs/themis/wiki/Objective-C-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/objc)
- Java / Android [documentation](https://github.com/cossacklabs/themis/wiki/Android-Howto)
- Ruby [documentation](https://github.com/cossacklabs/themis/wiki/Ruby-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/ruby)
- Python [documentation](https://github.com/cossacklabs/themis/wiki/Python-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/python)
- PHP [documentation](https://github.com/cossacklabs/themis/wiki/PHP-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/php)
- C++ [documentation](https://github.com/cossacklabs/themis/wiki/CPP-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/c%2B%2B)
- Javascript (NodeJS) [documentation](https://github.com/cossacklabs/themis/wiki/NodeJS-Howto) and [examples](https://github.com/cossacklabs/themis/tree/master/docs/examples/js)
- Go [documentation](https://github.com/cossacklabs/themis/wiki/Go-Howto)
- С++ PNaCl for Google Chrome in separate [WebThemis project](https://github.com/cossacklabs/webthemis)

# Availability

Themis supports the following architectures: x86/x64, armv*, various androids

It is checked to compile on:

* Debian 7.8, CentOS 6.6, CentOS Linux 7.1.1503, Ubuntu 14.04 LTS 
* MS Windows 7, 8, 10
* OSX 10.10—10.11
* Android 4.4.2
* Android 4.4.4 / CyanogenMod 11
* Android 5
* iOS7—iOS9+, x32/x64

We plan to expand this minuscule availability scope with broader set of platforms. If you'd like to help Themis arrive (or get better) on your favourite platform / language — get in touch.

# Tutorials

As long as it is feasible, we'll accumulate list of all tutorials we publish on how to use Themis in different cases here:

* [Releasing Themis into public: usability testing](https://www.cossacklabs.com/02-usability-testing.html), which goes a bit into how to use Secure Message for iOS and Python. Go directly into [corresponding github repository](https://github.com/cossacklabs/themis-ux-testing) to play with code. 
* [Building encrypted chat service with Themis and mobile websocket example](https://www.cossacklabs.com/building-secure-chat), which outlines stages necessary to build encrypted chat service around Ruby websocket server, with clients in iOS and Android. [Github repository](https://github.com/cossacklabs/mobile-websocket-example) with code for the post.

# Sample projects

During development, we frequently do Proof-of-Concept projects to test different assumptions. They serve as interesting demos of what Themis is capable of:

* 0fc anonymous web chat, pythemis (Python) + webthemis (C++ + HTML/JS): [github repo](https://github.com/cossacklabs/0fc) [blog post](https://cossacklabs.com/building-endtoend-webchat.html)
* sesto: secure storage, pythemis (Python) + webthemis (C++ + HTML/JS): [github repo](https://github.com/cossacklabs/sesto) [blog post](https://cossacklabs.com/presenting-sesto.html)

# Documentation

[Project's github wiki](https://www.github.com/cossacklabs/themis/wiki) contains ever-evolving official documentation, which contains everything from how to use it to ways to contribute to it, with a brief explanation of cryptosystems and architecture behind main Themis library in between. 
