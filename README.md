# federnd
A caching DNS forwarder that randomizes the resolvers

## Why are you making this?
1. I couldn't find any other server that could both cache and randomize the resolver target. (I did see [this post](https://www.ctrl.blog/entry/kresd-random-dns-forwarding.html) about adding randomization to knot-resolver, however that seems to break the caching functionality and no other client seems to support randomization)
2. It's an excuse to learn rust. So yes, there will be mistakes. Please be kind.

## What is with the name?
I thought of "bouncy" as aname as it will bounce between different resolvers. But there are a lot of projects already using that name. So I used the German translation as there weren't any github probjects with the name "federnd" and I also like how it has the traditional "d" for daemon suffix.

## Roadmap/Intended Features
- [x] Pick a license
  * MPL 2.0 seems to a good compromise between GPL and MIT
- [x] Initialize project
- [ ] Read yaml config file
- [ ] Basic DNS forwarding
- [ ] Tell Firefox (and other browsers?) not to use DOH
  - [ ] Configurable: default on
- [ ] Randomize resolver
- [ ] Cache responses
- [ ] Domain pinning
  * Requests for same domain will continue to use same resolver
  - [ ] Configurable: off, by domain (default), or by subdomain
- [ ] DNS over TLS (client) support
- [ ] DNS over HTTPS (client) support
- [ ] Use /etc/hosts or some other local/internal domain list
- [ ] Bind to specific interface
- [ ] Deprioritize/temporarily disable resolver if unresponsive
- [ ] Socks/tor proxy support
- [ ] Domain specific settings:
  - [ ] Domain priming
    * Domain will be automatically refreshed when TTL expires so it is always in cache
  - [ ] always use a specific resolver
  - [ ] use a specific proxy/tor
  - [ ] bind to specific interface
  - [ ] never cache
  - [ ] override TTL
 
