# Light weight implementations of real-time communication protocols and applications in Python

![rtclite](https://raw.githubusercontent.com/theintencity/rtclite/master/assets/logo-rtclite.png)

This project aims to create an open source repository of light weight implementations 
of real-time communication (RTC) protocols and applications.
In a nutshell, it contains reference implementations, 
prototypes and sample applications, mostly written in Python, of various RTC standards defined in 
the IETF, W3C and elsewhere, e.g., RFC 3261 (SIP), RFC 3550 (RTP), RFC 3920 (XMPP), RTMP, etc.


## Background

> This project was migrated from <https://code.google.com/p/rtclite> on May 17, 2015  
> Keywords: *Python*, *Realtime*, *Communication*, *Library*, *Academic*, *SIP*, *RTP*, *WebRTC*, *RTMP*  
> Members: *kundan10*, *theintencity*, *mamtasingh05*, *voipresearcher*  
> Links: [Project](http://39peers.net/), [Support](http://groups.google.com/group/myprojectguide)  
> License: [GNU Lesser GPL](http://www.gnu.org/licenses/lgpl.html)  

The "rtclite" project is created to host the source code of the "39 peers"
project, and the two project names are used interchangeably here.
Please visit the [project website](http://39peers.net) for further details.

This project is an effort to unify my Python-based projects related to SIP, RTP, RTMP, Web
into a single theme of real-time communication (RTC). In particular, the initial source code
is borrowed after cleanup from these projects, without adding any significant new functionality:

> [p2p-sip](https://github.com/theintencity/p2p-sip): SIP, P2P, XMPP and other related code.
> [rtmplite](https://github.com/theintencity/rtmplite): RTMP, RTMFP and SIP-RTMP translation.
> [restlite](https://github.com/theintencity/restlite): REST web APIs

## Motivation

The primary motivation is described in my earlier blog article,
[a proposal for reference implementation repositiory for RFCs](http://blog.kundansingh.com/2011/06/proposal-for-reference-implementation.html).

With growing number of emerging RTC standards, the trend of
creating specifications without implementations, and consecutively the interoperability
problems have increased. This project will hopefully simplify the
job of an RTC programmer and, in the long term, will result in more interoperable
and robust RTC products.
This project contains source code of various RTC specifications.
The source code is annotated with text snippets from
the relevant specification to show (a) how the code fragment implements
the specification, (b) which part of the specification is relevant to the
code fragment, and vice-versa, and (c) the implicit code documentation 
borrowed from the text in the specification.

[Click to browse the annotated source code](http://kundansingh.com/p/rtclite/index.html).

Alternatively, click on individual modules below to view that annotated code and its Python source lines of code (SLoC). The SLoC also shows the concise nature of this Python implementation of various protocols and applications. 

| Module | Package or Description | SLoC |
|:------|:------|-----:|
|| package: rtclite.std.ietf ||
|[rfc1035](http://kundansingh.com/p/rtclite/std/ietf/rfc1035.py.html)| DNS lookup for any record type |1125|
|[rfc2198](http://kundansingh.com/p/rtclite/std/ietf/rfc2198.py.html)| RTP payload type for redundant audio data |51|
|[rfc2396](http://kundansingh.com/p/rtclite/std/ietf/rfc2396.py.html)| Various forms of addresses such as URI or SIP address |177|
|[rfc2617](http://kundansingh.com/p/rtclite/std/ietf/rfc2617.py.html)| HTTP basic and digest authentication |92|
|[rfc2833](http://kundansingh.com/p/rtclite/std/ietf/rfc2833.py.html)| DTMF touch-tone payload in RTP packet |48|
|[rfc3261](http://kundansingh.com/p/rtclite/std/ietf/rfc3261.py.html)| **Session Initiation Protocol (SIP)** |1425|
|[rfc3263](http://kundansingh.com/p/rtclite/std/ietf/rfc3263.py.html)| SIP server discovery using DNS NAPTR, SRC and A records |107|
|[rfc3264](http://kundansingh.com/p/rtclite/std/ietf/rfc3264.py.html)| SDP offer-answer model for unicast session in SIP |97|
|[rfc3489](http://kundansingh.com/p/rtclite/std/ietf/rfc3489.py.html)| Basic NAT traversal technologies such as STUN, NAT discovery using STUN and TURN |595|
|[rfc3550](http://kundansingh.com/p/rtclite/std/ietf/rfc3550.py.html)| **Real-time Transport Protocol (RTP)** and companion control protocol RTCP |725|
|[rfc3551](http://kundansingh.com/p/rtclite/std/ietf/rfc3551.py.html)| Static payload types for RTP |34|
|[rfc3920](http://kundansingh.com/p/rtclite/std/ietf/rfc3920.py.html)| XMPP core for client side |351|
|[rfc3921](http://kundansingh.com/p/rtclite/std/ietf/rfc3921.py.html)| IM and presence of XMPP client side |290|
|[rfc4566](http://kundansingh.com/p/rtclite/std/ietf/rfc4566.py.html)| Session Description Protocol (SDP) |148|
|[rfc5389](http://kundansingh.com/p/rtclite/std/ietf/rfc5389.py.html)| Session traversal utilities for NAT (STUN) |128|
|[rfc6455](http://kundansingh.com/p/rtclite/std/ietf/rfc6455.py.html)| WebSocket protocol - client and server |565|
|[rfc7064](http://kundansingh.com/p/rtclite/std/ietf/rfc7064.py.html)| URI scheme for STUN, patch rfc2396 |28|
|[rfc7065](http://kundansingh.com/p/rtclite/std/ietf/rfc7065.py.html)| URI scheme for TURN, patch rfc2396 |41|
|| package: rtclite.std.itu_t ||
|[t140](http://kundansingh.com/p/rtclite/std/itu_t/t140.py.html)| real-time text (RTT) payload in RTP |13|
|| package: rtclite.std.w3c ||
|[simplexml](http://kundansingh.com/p/rtclite/std/w3c/simplexml.py.html)| Simple XML DOM with Pythonic convenient methods and operators for XML and XMLList |363|
|| package: rtclite.app.sip ||
|[client](http://kundansingh.com/p/rtclite/app/sip/client.py.html)| SIP user agent library for registration, call, IM, conferences |1258|
|[server](http://kundansingh.com/p/rtclite/app/sip/server.py.html)| Very simple SIP registration, proxy server, including WebSocket  |100|
|[caller](http://kundansingh.com/p/rtclite/app/sip/caller.py.html)| **command line SIP caller** and call listener with voice, TTS, ASR, DTMF |729|
|[api](http://kundansingh.com/p/rtclite/app/sip/api.py.html)| SIP API for use in programmable servers and clients |371|
|[p2p](http://kundansingh.com/p/rtclite/app/sip/p2p.py.html)| One way to implement P2P-SIP, not based on the IETF standard |315|
|| package: rtclite.app.net.p2p ||
|[dht](http://kundansingh.com/p/rtclite/app/net/p2p/dht.py.html)| Distributed Hash Table (DHT) inspired by BambooDHT and OpenDHT |1712|
|[dhtgui](http://kundansingh.com/p/rtclite/app/net/p2p/dhtgui.py.html)| GUI to see P2P network in action |356|
|[opendht](http://kundansingh.com/p/rtclite/app/net/p2p/opendht.py.html)| (defunct) Interface to connect to OpenDHT |63|
|[pipe](http://kundansingh.com/p/rtclite/app/net/p2p/pipe.py.html)| P2P pipe abstraction |590|
|| package: rtclite.app.sec ||
|[crypto](http://kundansingh.com/p/rtclite/app/sec/crypto.py.html)| Crypto library wrapper, e.g., PKI, ASN1, ARC, etc. |251|
|[dummycrypto](http://kundansingh.com/p/rtclite/app/sec/dummycrypto.py.html)| Stub for crypto module |24|
|| package: rtclite.app.web.rest ||
|[base](http://kundansingh.com/p/rtclite/app/web/rest/base.py.html)| Building blocks for creating REST APIs |196|
|[data](http://kundansingh.com/p/rtclite/app/web/rest/data.py.html)| Expose structured data as REST resources |152|
|[files](http://kundansingh.com/p/rtclite/app/web/rest/files.py.html)| Expose local file structure as REST resources |94|
|| package: rtclite.app.web.rtc ||
|[notify](http://kundansingh.com/p/rtclite/app/web/rtc/notify.py.html)| WebRTC notification server for signaling over WebSocket |198|
|| package: rtclite.vnd.adobe ||
|[rtmp](http://kundansingh.com/p/rtclite/vnd/adobe/rtmp.py.html)| **Real Time Messaging Protocol (RTMP)** parsing, formatting, server, and FLV |1068|
|[rtmpclient](http://kundansingh.com/p/rtclite/vnd/adobe/rtmpclient.py.html)| command line RTMP client |345|
|[rtmpt](http://kundansingh.com/p/rtclite/vnd/adobe/rtmpt.py.html)| RTMP tunneling |165|
|[siprtmp](http://kundansingh.com/p/rtclite/vnd/adobe/siprtmp.py.html)| SIP-RTMP translation for voice and video |1147|
|[aes](http://kundansingh.com/p/rtclite/vnd/adobe/aes.py.html)| Pure python based AES, used only when PyOpenSSL is not found |179|
|[amf](http://kundansingh.com/p/rtclite/vnd/adobe/amf.py.html)| Action Message Format (AMF) 0 and 3 |367|
|[rtmfp](http://kundansingh.com/p/rtclite/vnd/adobe/rtmfp.py.html)| Real-Time Media Flow Protocol (RTMFP) parsing and formatting |2095|
|| package: rtclite.vnd.google ||
|[chat](http://kundansingh.com/p/rtclite/vnd/google/chat.py.html)| **Send and receive Google Chat messages** over XMPP |60|
|| package: rtclite ||
|[common](http://kundansingh.com/p/rtclite/common.py.html)| Common utility methods and classes |410|
|[multitask](http://kundansingh.com/p/rtclite/multitask.py.html)| Co-operative multitasking |469|


Furthermore, the project contains various applications built on top of these
open standards and open source implementations to demonstrate real use cases, e.g.,
SIP proxy server, XMPP client, command line SIP dialer, SIP-RTMP gateway, etc.
The light-weight nature of the various Python modules enables other developers to
easily use these in their projects, without other complex framework dependencies.

## Design Goals

The primary design goal of this project is to provide reference implementation
of popular real-time communication protocols. The implementation is done in
Python 2.7 programming language, but may be ported in future to others. There are
two parts in the source code -- the protocols and
the applications.
Following goals are met in the current implementations of the protocols.

* System Portability: apart from the Python standard library, the
  project should not rely on other third-party libraries. If such third-
  party libraries become necessary, consider including them in the
  repository or provide clear instructions for such dependency.
  The module should isolate such dependencies to smaller part if possible.
  The project should therefore be portable to many interpreters and
  runtime environments.
* Threading: threading vs event-driven programming style is decision that
  best left to the application developer instead of forcing a particular
  choice in the library. The project should not impose such decision in
  reference implementation. If it is necessary to include such choice,
  then it should provide reasonable set of alternatives pre-built in the
  module.
* Concise and Precise Code: Python enables expressing ideas in code in
  less number of lines. The programmer should further honor the Pythonic
  programming style. Less number of lines means that one can write software
  faster, and with less garbage (syntactic sugar), one can read and
  understand the code easily. Moreover, testing and review efforts are less.
  The resulting improvement in programmer's efficiency reflects in her
  motivation to write more clean code.
* Testing: testing is an integral part of all code in this project. It
  uses doctest whereever possible to integrate code with documentation and
  testing. Alternatively, dedicated test and sample applications are
  included for manual or automated testing. Generally, running a protocol module
  on command line via Python interpreter should run its test cases and
  report any errors.
* Logging: standard logging module is used at various log levels. The code
  should avoid using the standard print statements as much as possible
  for logging - helps in migrating to Python3 in future, and reduces
  unwanted output when the module is included elsewhere.

On the other hand, implementation of an application may depend on
the specific system, e.g., for audio/video interface, or specific threading vs. event
programming style, or custom user interface, e.g., web vs. curses vs. command line.
These applications are for demonstration purpose, and not for production use.

## Software Structure

The `std`, `app` and `vnd` packages under top-level `rtclite` include the implementations
of the protocols and the applications. The `std` package further includes sub-packages
for standard bodies, e.g., `ietf` and `w3c`. The `app` package contains not only the
applications but also supporting library modules classified under high level
categories such as `net`, `sip` or `sec`, and the `vnd` package contains vendor specific 
protocol implementations such as `adobe` sub-package for `rtmp` and `siprtmp`.

In an application, a module from this project should always be imported with the
package hierarchy, e.g.,
```
import rfc3261 # WRONG
from rtclite.std.ietf import rfc3261 # RIGHT
from rtclite.std.ietf.rfc3261 import UserAgent # RIGHT AGAIN
import rtclite.std.ietf.rfc3261 # STILL RIGHT
```

Similarly, a protocol or application module should be invoked with the right package
hierarchy, e.g.,
```
cd rtclite/std/ietf; python rfc3921.py  # WRONG
python -m rtclite.std.ietf.rfc3921 # RIGHT
```

The included `Makefile` can be used on Unix-like systems to test all the protocol
modules, to generate annotated source file documentations, and to create
installable distribution.
```
make test
make doc
```
## License and contributions

Please see [LICENSE](/LICENSE) for details on software license and copyright. 
In particular, this software is available as either LGPL or alternative license. 
Any other contributors, who submit code or patches to this project
automatically transfer the copyright of their work to the original author. 
This allows the original author to create derivative work or issue alternative 
license outside of LGPL.
