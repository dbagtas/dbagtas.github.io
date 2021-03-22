---
layout: essay
type: essay
title: What to expect from HTTP/3
# All dates must be YYYY-MM-DD format!
date: 2021-03-17
labels:
  - Website Development
---

<img class="ui tiny right spaced image" src="../images/degree_difficulty.jpg">TypeScript doesn't have the rich set of native collection classes that you're used to in the .NET Framework -- instead, it has just arrays and tuples. Fortunately, you can do quite a lot with them.

We barely deployed HTTP/2 and we are already talking about HTTP/3. The web is moving very fast these days and its users will benefit from that. In fact, Chrome is already using HTTP/3 if you are connecting to Google’s servers. The protocol has been in development and tested in production environment for years under the name of QUIC. It suppresses TCP and is built up entirely on UDP. And the best in the end – encryption is mandatory (at least for the time being).

## Isolated Streams

HTTP/2 introduced multiplexing, which is useful, because it allows transfer­ring of multiple streams over a single connection. But when one of those streams lost a single packet, the whole connection prevents progress on all its streams. It’s a limitation of TCP which wasn't intended to use multiple streams. Therefore HTTP/3 introduced whole new stack on the top of UDP. A lost packet affects only the stream in that packet. Other streams can continue to progress.

## Persistent Connection

Running long running connections will be finally possible when your device is mobile.

## NAT Rebinding

In the IPv4 world, a single IP address can have multiple web­servers behind it. The problem is that when you establish a connection the second web­server behind the NAT, the first connection will time­out because the source port of your IP address has changed.

QUIC will establish only one connection to NAT and endpoints will be responsible for identifying connections. This concept is called connection ID.

## Connection Migration

Currently, when the device switches from LTE network to Wi-Fi, the old connection is lost, and new connection must be established. HTTP/3 will offer a migration of the connections to different IP address.

## Backward Compatibility

The approach is like HSTS mechanism. First, the browser establishes the connection in HTTP 1.1 or HTTP/2 protocol. Second, the server responds with Alt-Svc header. Third, the browser will switch to QUIC and use it in the future.

## Privacy

Privacy is a compromise between usability and security. The bar of security rising.

## Always Encrypted

TLS 1.3 encryption is mandatory. Yes, the second at­tempt. Let's see if it won't be removed for “performance” reasons.

## Deflecting Reflection

Reflection attacks are based on spoofing victim’s IP address after being compromised. QUIC protocol defines an explicit source-address verification mechanism.
