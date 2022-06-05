mixed-port: 7890
allow-lan: true
mode: Rule
log-level: info
external-controller: 127.0.0.1:9090
dns:
  enable: true
  ipv6: false
  enhanced-mode: redir-host
  default-nameserver:
    - 8.8.8.8
    - 1.1.1.1
  nameserver:
    - https://dns.google/dns-query
    - https://1.1.1.1/dns-query
  fallback:
    - https://dns.google/dns-query
    - https://1.1.1.1/dns-query
  fallback-filter:
    geoip: true
proxies:

  
  - {name: YouTube 📛 Tohid, server: 95.111.255.137, port: 443, type: ss, cipher: chacha20-ietf-poly1305, password: "2Ato4vCSX6eX", udp: true} 
  
  - {name: NL 🇳🇱 Haarlem, server: 51.15.0.113, port: 989, type: ss, cipher: aes-256-cfb, password: "f8f7aCzcPKbsF8p3", udp: true}
  
  - {name: ITA 🇮🇹 Milan, server: 95.174.23.218,  port: 989, type: ss, cipher: aes-256-cfb, password: "f8f7aCzcPKbsF8p3", udp: true} 
  
  - {name: HUN 🇭🇺 Budapest, server: 194.71.130.160, port: 989, type: ss, cipher: aes-256-cfb, password: "f8f7aCzcPKbsF8p3", udp: true}
  
  - {name: GRC 🇬🇷 Athens, server: 185.243.214.55, port: 50003, type: ss, cipher: aes-256-cfb, password: "8460400130", udp : true}
  
  - {name: GER 🇩🇪 Frankfurt, server: 193.108.117.24, port: 6679, type: ss, cipher: aes-256-gcm, password: "TEzjfAYq2IjtuoS",  udp: true}
  
  - {name: AZR 🇦🇿 Baku, server: 94.20.154.38, port: 50000, type: ss, cipher: aes-256-cfb, password: "3135771619", udp: true}
  
  - {name: USA 🇺🇸 Dallas, server: 38.86.135.36, port: 6679, type: ss, cipher: aes-256-gcm, password: "TEzjfAYq2IjtuoS", udp: true}
  
  - {name: NOR 🇳🇴 Oslo, server: 5.183.100.87, port: 50003, type: ss, cipher: aes-256-cfb, password: "8460400130", udp: true}
  
  - {name: UK 🇺🇦 Kyiv, server: 77.247.125.27, port: 50003, type: ss, cipher: aes-256-cfb, password: "8460400130", udp: true}
  
  - {name: TUR 🇹🇷 Istanbul, server: 185.219.134.52, port: 50003, type: ss, cipher: aes-256-cfb, password: "8460400130", udp: true}
  
  - {name: FRA 🇫🇷 Paris, server: 195.154.200.150, port: 2376, type: ss, cipher: aes-256-gcm, password: "faBAoD54k87UJG7", udp: true}
  
  - {name: UK 🇬🇧 London, server: 'uk.london1.vpntester.net', port: 15256, type: ss, cipher: chacha20-ietf-poly1305, password: "4SGLMZ7Z83fN", udp: true}
  
  - {name: CAN 🇨🇦 Richmond Hill, server: 198.57.27.184, port: 6679, type: ss, cipher: aes-256-gcm, password: "TEzjfAYq2IjtuoS", udp: true}
  
  - {name: Tohid, server: 'asr-farda.ir', port: 80, type: vmess, uuid: 63af13a9-df13-11ec-abe3-f18437f70dfe, alterId: 0, udp: true, tls: false, skip-cert-verify: false, network: ws, ws-path: /EvMchy69/, cipher: auto, ws-host: my.mci.ir} 
 
  - {name: Tohid2, server: 'asr-farda.ir', port: 80, type: vmess, uuid: 63af13a9-df13-11ec-abe3-f18437f70dfe, alterId: 0, udp: false, tls: false, skip-cert-verify: false, network: ws, ws-path: /EvMchy69/, cipher: auto, ws-host: my.mci.ir}
proxy-groups:
  - name: 🔆 LIST 🔆
    type: select
    proxies:
      - ♻️ AUTO All ♻️
      - ♻️ AUTO AMERICAS ♻️
      - ♻️ AUTO ASIA ♻️
      - ♻️ AUTO EUROPE ♻️
      - ♻️ AUTO OTHERS ♻️
      - 🔰 Tohid 🔰
  - name: 🔰 Tohid 🔰
    type: select
    proxies:
      - Tohid
      - Tohid2
      - Nim-YouTube 📛 Tohid
      - Nim-HUN 🇭🇺 Budapest
      - Nim-ITA 🇮🇹 Milan
      - Nim-NL 🇳🇱 Haarlem
      - Nim-AZR 🇦🇿 Baku
      - Nim-GER 🇩🇪 Frankfurt
      - Nim-GRC 🇬🇷 Athens
      - Nim-UK 🇺🇦 Kyiv
      - Nim-NOR 🇳🇴 Oslo
      - Nim-USA 🇺🇸 Dallas
      - Nim-CAN 🇨🇦 Richmond Hill
      - Nim-FRA 🇫🇷 Paris
      - Nim-TUR 🇹🇷 Istanbul
      - Nim-UK 🇬🇧 London
   
  - name: ♻️ AUTO ASIA ♻️
    type: url-test
    proxies:
      - Nim-HUN 🇭🇺 Budapest
      - Nim-TUR 🇹🇷 Istanbul
      - Nim-AZR 🇦🇿 Baku

    url: 'https://github.com/zhukov/webogram'
    interval: 300    
  
  - name: ♻️ AUTO All ♻️
    type: url-test
    proxies:

      - Nim-YouTube 📛 Tohid
      - Nim-HUN 🇭🇺 Budapest
      - Nim-ITA 🇮🇹 Milan
      - Nim-NL 🇳🇱 Haarlem
      - Nim-AZR 🇦🇿 Baku
      - Nim-GER 🇩🇪 Frankfurt
      - Nim-GRC 🇬🇷 Athens
      - Nim-UK 🇺🇦 Kyiv
      - Nim-NOR 🇳🇴 Oslo
      - Nim-USA 🇺🇸 Dallas
      - Nim-FRA 🇫🇷 Paris
      - Nim-TUR 🇹🇷 Istanbul
      - Nim-UK 🇬🇧 London

    url: 'https://github.com/zhukov/webogram'
    interval: 300
  - name: ♻️ AUTO AMERICAS ♻️
    type: url-test
    proxies:
 
      - Nim-USA 🇺🇸 Dallas
      - Nim-CAN 🇨🇦 Richmond Hill
      
      
    url: 'https://github.com/zhukov/webogram'
    interval: 300
  - name: ♻️ AUTO EUROPE ♻️
    type: url-test
    proxies:
      - Nim-YouTube 📛 Tohid
      - Nim-ITA 🇮🇹 Milan
      - Nim-NL 🇳🇱 Haarlem
      - Nim-AZR 🇦🇿 Baku
      - Nim-GER 🇩🇪 Frankfurt
      - Nim-GRC 🇬🇷 Athens
      - Nim-UK 🇺🇦 Kyiv
      - Nim-UK 🇬🇧 London
      - Nim-FRA 🇫🇷 Paris
      - Nim-NOR 🇳🇴 Oslo
    url: 'https://github.com/zhukov/webogram'
    interval: 300
  - name: ♻️ AUTO OTHERS ♻️
    type: url-test
    proxies:
      - Nim-YouTube 📛 Tohid
      - Nim-HUN 🇭🇺 Budapest
      - Nim-ITA 🇮🇹 Milan
      - Nim-NL 🇳🇱 Haarlem
      - Nim-AZR 🇦🇿 Baku
      - Nim-GER 🇩🇪 Frankfurt
      - Nim-GRC 🇬🇷 Athens
      - Nim-UK 🇺🇦 Kyiv
      - Nim-NOR 🇳🇴 Oslo
      - Nim-USA 🇺🇸 Dallas
      - Nim-CAN 🇨🇦 Richmond Hill
      - Nim-FRA 🇫🇷 Paris
      - Nim-TUR 🇹🇷 Istanbul
      - Nim-UK 🇬🇧 London
    url: 'https://github.com/zhukov/webogram'
    interval: 300
 
  - name: "Auto-Fallback"
    type: fallback
    proxies:

      - Nim-YouTube 📛 Tohid
      - Nim-HUN 🇭🇺 Budapest
      - Nim-ITA 🇮🇹 Milan
      - Nim-NL 🇳🇱 Haarlem
      - Nim-AZR 🇦🇿 Baku
      - Nim-GER 🇩🇪 Frankfurt
      - Nim-GRC 🇬🇷 Athens
      - Nim-UK 🇺🇦 Kyiv
      - Nim-NOR 🇳🇴 Oslo
      - Nim-USA 🇺🇸 Dallas
      - Nim-CAN 🇨🇦 Richmond Hill
      - Nim-FRA 🇫🇷 Paris
      - Nim-TUR 🇹🇷 Istanbul
      - Nim-UK 🇬🇧 London
    url: 'https://github.com/zhukov/webogram'
    interval: 300

  - name: "Nim-YouTube 📛 Tohid"
    type: relay
    proxies:
      - Tohid2
      - YouTube 📛 Tohid
  - name: "Nim-HUN 🇭🇺 Budapest"
    type: relay
    proxies:
      - Tohid
      - HUN 🇭🇺 Budapest        
  - name: "Nim-ITA 🇮🇹 Milan"
    type: relay
    proxies:
      - Tohid2
      - ITA 🇮🇹 Milan          
  - name: "Nim-NL 🇳🇱 Haarlem"
    type: relay
    proxies:
      - Tohid
      - NL 🇳🇱 Haarlem
  - name: "Nim-AZR 🇦🇿 Baku"
    type: relay
    proxies:
      - Tohid2
      - AZR 🇦🇿 Baku            
  - name: "Nim-GER 🇩🇪 Frankfurt"
    type: relay
    proxies:
      - Tohid
      - GER 🇩🇪 Frankfurt          
  - name: "Nim-GRC 🇬🇷 Athens"
    type: relay
    proxies:
      - Tohid2
      - GRC 🇬🇷 Athens          
  - name: "Nim-UK 🇺🇦 Kyiv"
    type: relay
    proxies:
      - Tohid2
      - UK 🇺🇦 Kyiv 
  - name: "Nim-NOR 🇳🇴 Oslo"
    type: relay
    proxies:
      - Tohid
      - NOR 🇳🇴 Oslo  
  - name: "Nim-USA 🇺🇸 Dallas"
    type: relay
    proxies:
      - Tohid2
      - USA 🇺🇸 Dallas         
  - name: "Nim-CAN 🇨🇦 Richmond Hill"
    type: relay
    proxies:
      - Tohid2
      - CAN 🇨🇦 Richmond Hill             
  - name: "Nim-UK 🇬🇧 London"
    type: relay
    proxies:
      - Tohid
      - UK 🇬🇧 London 
  - name: "Nim-TUR 🇹🇷 Istanbul"
    type: relay
    proxies:
      - Tohid2
      - TUR 🇹🇷 Istanbul    
  - name: "Nim-FRA 🇫🇷 Paris"
    type: relay
    proxies:
      - Tohid
      - FRA 🇫🇷 Paris

