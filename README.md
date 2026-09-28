# Padavan-clash

<img width="696" height="792" alt="image" src="https://github.com/user-attachments/assets/8bff9671-e59f-4eaa-8e4e-5eda048ff064" />

<img width="692" height="884" alt="image" src="https://github.com/user-attachments/assets/e0ed6659-2eb4-4661-b529-34dbc3f6f6ca" />

### 点这里自定义 clash dns 或其他配置：

unified-delay: true

tun:
  enable: false
  stack: gvisor
  dns-hijack:
    - 8.8.8.8:53
    - 1.1.1.1:53
  auto-route: false
  auto-detect-interface: false

dns:
  cache-algorithm: arc
  enable: true
  ipv6: false
  listen: 0.0.0.0:8053
  default-nameserver:
    - tcp://8.8.8.8:53
  enhanced-mode: fake-ip
  use-hosts: true
  
  #配置不使用fake-ip的域名（防回环过滤）
  fake-ip-filter:
    - '*.lan'
    - localhost.ptlogin2.qq.com
    - '+.msftconnecttest.com'
    - '+.msftncsi.com'
    - 'localhost'
    - '*.local'
    - '+.stun.*'
    - '+.stun1.*'
    - '+.stun2.*'
    - '+.stun3.*'
    - '+.stun4.*'
    - '+.ntp.*'

  respect-rules: true
  proxy-server-nameserver:
    - tcp://8.8.8.8:53
  nameserver:
    - 223.5.5.5
    - 114.114.114.114
    - 119.29.29.29

  fallback:
    - https://dns.google/dns-query
    - https://1.0.0.1/dns-query
    - tcp://8.8.8.8:53
    - tcp://8.8.4.4:53
    - tcp://208.67.222.222:443
    - tcp://208.67.220.220:443

  fallback-filter:
    geoip: true
    geoip-code: CN
    ipcidr:
      - 240.0.0.0/4
    domain:
      - '+.google.com'
      - '+.googleapis.com'
      - '+.youtube.com'
      - '+.appspot.com'
      - '+.telegram.com'
      - '+.facebook.com'
      - '+.twitter.com'
      - '+.blogger.com'
      - '+.gmail.com'
      - '+.gvt1.com'

experimental:
  quic-go-disable-gso: true
  quic-go-disable-ecn: true
  dialer-ip4p-convert: false

sniffer:
  enable: true
  override-destination: true
  sniff:
    http: { ports: [80, 8080] }
    tls: { ports: [443, 8443] }
  skip-domain:
    - 'courier.push.apple.com'
    - 'Mijia Cloud'


<img width="757" height="699" alt="image" src="https://github.com/user-attachments/assets/8c8ee599-8a0d-4b34-8a84-6d30e3813bab" />

<img width="758" height="825" alt="image" src="https://github.com/user-attachments/assets/2763bd78-b8a4-44a4-9fd4-1cd6d8623f23" />


<img width="630" height="953" alt="image" src="https://github.com/user-attachments/assets/15a62d35-8e03-4266-b286-796f42a5bc04" />



