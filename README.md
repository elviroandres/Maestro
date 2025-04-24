# Maestro

No teste efetuado Origem: 19988283975
                  Destino: 3121730041

Temos que no Session Progress encaminhado para o IP da OI foi com o campo **o=UC2B 1745452016 1745452017 IN IP4 189.113.38.48 **

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


Após o avanço na sinalização o SBC recebeu e repassou o **200 OK**  do atendimento se alterações no campo **o=**

```text
send 1269 bytes to tls/[200.97.114.118]:5061 at 11:40:59.893900:
------------------------------------------------------------------------
SIP/2.0 200 OK
Via: SIP/2.0/TLS 200.97.114.118:5061;branch=z9hG4bKlohb7n306gr5fcsbsqj0.1;rport=5061
From: <sip:19988283975@10.225.121.8:5061;user=phone>;tag=pBer115cQDZ6Q
To: 3121730041 <sip:3121730041@10.225.111.6;gw=3121730041>;tag=yNvcy2057yKcK
Call-ID: f443b72c-9bbc-123e-c9a8-000c29f15bb8
CSeq: 1029290518 INVITE
Contact: <sip:3121730041@189.113.38.48:5061;transport=tls>
User-Agent: UC2B - 1.10.5-release~64bit
Allow: INVITE, ACK, BYE, CANCEL, OPTIONS, MESSAGE, INFO, UPDATE, REGISTER, REFER, NOTIFY, PUBLISH, SUBSCRIBE
Require: timer
Supported: timer, path, replaces
Allow-Events: talk, hold, conference, presence, as-feature-event, dialog, line-seize, call-info, sla, include-session-description, presence.winfo, message-summary, refer
Session-Expires: 1800;refresher=uac
Content-Type: application/sdp
Content-Disposition: session
Content-Length: 292
Remote-Party-ID: "Outbound Call" <sip:3121730041@10.225.111.6>;party=calling;privacy=off;screen=no

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

2025-04-24 11:40:59.885395 [DEBUG] switch_channel.c:3870 (sofia/internal/19988283975@10.225.121.8:5061) Callstate Change EARLY -> ACTIVE
2025-04-24 11:40:59.885395 [DEBUG] sofia.c:7327 Channel sofia/internal/19988283975@10.225.121.8:5061 entering state [completed][200]
2025-04-24 11:40:59.885395 [DEBUG] switch_ivr_originate.c:3852 Originate Resulted in Success: [sofia/external/3121730041]
2025-04-24 11:40:59.885395 [DEBUG] switch_ivr_bridge.c:1793 (sofia/external/3121730041) State Change CS_CONSUME_MEDIA -> CS_EXCHANGE_MEDIA
2025-04-24 11:40:59.885395 [DEBUG] switch_core_state_machine.c:585 (sofia/external/3121730041) Running State Change CS_EXCHANGE_MEDIA (Cur 38 Tot 568815)
2025-04-24 11:40:59.885395 [DEBUG] switch_core_state_machine.c:654 (sofia/external/3121730041) State EXCHANGE_MEDIA
2025-04-24 11:40:59.885395 [DEBUG] mod_sofia.c:656 SOFIA EXCHANGE_MEDIA
2025-04-24 11:40:59.905403 [DEBUG] switch_rtp.c:7759 Correct audio ip/port confirmed.
```

Finalmente o SBC recebe uma sequencia de **ACK e BYE do IP da 200.97.114.118**

```text
recv 519 bytes from tls/[200.97.114.118]:5061 at 11:40:59.919549:
------------------------------------------------------------------------
ACK sip:3121730041@189.113.38.48:5061;transport=tls SIP/2.0
Via: SIP/2.0/TLS 200.97.114.118:5061;branch=z9hG4bKkmfuka10b0voqp6rv060.1
Max-Forwards: 69
From: <sip:19988283975@10.225.121.8:5061;user=phone>;tag=pBer115cQDZ6Q
To: 3121730041 <sip:3121730041@10.225.111.6;gw=3121730041>;tag=yNvcy2057yKcK
Call-ID: f443b72c-9bbc-123e-c9a8-000c29f15bb8
CSeq: 1029290518 ACK
Content-Length: 0
P-Charging-Vector: icid-value=94es2086g1csiss6e9c23qo5h9cgjhtdibpqiqdcd1t4nn1e9rou6c3h52e1;icid-generated-at=200.97.114.118


recv 832 bytes from tls/[200.97.114.118]:5061 at 11:40:59.980379:
------------------------------------------------------------------------
BYE sip:3121730041@189.113.38.48:5061;transport=tls SIP/2.0
Via: SIP/2.0/TLS 200.97.114.118:5061;branch=z9hG4bKkmfuka10b0voqp6rv060cdt9mkrb0.1
Max-Forwards: 69
From: <sip:19988283975@10.225.121.8:5061;user=phone>;tag=pBer115cQDZ6Q
To: 3121730041 <sip:3121730041@10.225.111.6;gw=3121730041>;tag=yNvcy2057yKcK
Call-ID: f443b72c-9bbc-123e-c9a8-000c29f15bb8
CSeq: 1029290519 BYE
Contact: <sip:19988283975@200.97.114.118:5061;user=phone;transport=tls>
User-Agent: Vectura SoftSwitch C5
Allow: INVITE, ACK, BYE, CANCEL, OPTIONS, PRACK, UPDATE, INFO, NOTIFY, REFER, REGISTER, SUBSCRIBE
Supported: replaces, timer, 100rel, norefersub
Reason: Q.850;cause=41;text="Temporary failure"
Content-Length: 0
P-Charging-Vector: icid-value=94es2086g1csiss6e9c23qo5h9cgjhtdibpqiqdcd1t4nn1e9rou6c3h52e1;icid-generated-at=200.97.114.118
```

