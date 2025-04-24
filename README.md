# Maestro

No teste efetuado Origem: 19988283975
                  Destino: 3121730041

Temos que o 200 OK encaminha para o IP da OI 

```text
send 1252 bytes to tls/[200.97.114.118]:5061 at 11:40:48.715245:
------------------------------------------------------------------------
SIP/2.0 183 Session Progress
Via: SIP/2.0/TLS 200.97.114.118:5061;branch=z9hG4bKlohb7n306gr5fcsbsqj0.1;rport=5061
From: <sip:19988283975@10.225.121.8:5061;user=phone>;tag=pBer115cQDZ6Q
To: 3121730041 <sip:3121730041@10.225.111.6;gw=3121730041>;tag=yNvcy2057yKcK
Call-ID: f443b72c-9bbc-123e-c9a8-000c29f15bb8
CSeq: 1029290518 INVITE
Contact: <sip:3121730041@189.113.38.48:5061;transport=tls>
User-Agent: UC2B - 1.10.5-release~64bit
Accept: application/sdp
Allow: INVITE, ACK, BYE, CANCEL, OPTIONS, MESSAGE, INFO, UPDATE, REGISTER, REFER, NOTIFY, PUBLISH, SUBSCRIBE
Supported: timer, path, replaces
Allow-Events: talk, hold, conference, presence, as-feature-event, dialog, line-seize, call-info, sla, include-session-description, presence.winfo, message-summary, refer
Content-Type: application/sdp
Content-Disposition: session
Content-Length: 292
Remote-Party-ID: "3121730041" <sip:3121730041@10.225.111.6>;party=calling;privacy=off;screen=no

v=0
o=UC2B 1745452016 1745452017 IN IP4 189.113.38.48
s=UC2B
c=IN IP4 189.113.38.48
t=0 0
m=audio 53632 RTP/SAVP 8 99
a=rtpmap:8 PCMA/8000
a=rtpmap:99 telephone-event/8000
a=fmtp:99 0-16
a=ptime:20
a=crypto:1 AES_CM_128_HMAC_SHA1_80 inline:FPBlVxcagG0XhnoCdaHohcYaRHswd23/IKU79EzK

2025-04-24 11:40:48.725401 [DEBUG] sofia.c:7327 Channel sofia/internal/19988283975@10.225.121.8:5061 entering state [early][183]
2025-04-24 11:40:48.725401 [WARNING] switch_rtp.c:9005 Generating RTP locally but timestamp passthru is configured, disabling....
```
