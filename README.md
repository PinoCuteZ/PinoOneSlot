# PinoOneSlot
[general]
udp_whitelist=53, 1024-65535

[dns]
no-system
doh-server=https://ios.dns.nextdns.io/
server=8.8.8.8
server=1.1.1.1
server=45.90.28.0
server=45.90.30.0

[policy]

static=Wifi, Trực tiếp, VPN, Tự Chọn, img-url=wifi.system
static=4G, Trực tiếp, VPN, Tự Chọn, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Cellular.png
static=Chặn Ads, BẬT, TẮT, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Advertising.png
static=Chặn Quảng Cáo FB, TẮT, BẬT, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Facebook.png
static=Chặn OTA, TẮT, BẬT, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Apple_Update.png

static=Trực tiếp, direct, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/WiFi.png
static=VPN, proxy, img-url=network.system
url-latency-benchmark=Tự Chọn, server-tag-regex=., check-interval=600, tolerance=0, img-url=paperplane.fill.system
static=BẬT, reject, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Direct.png
static=TẮT, direct, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Reject.png
ssid=End, 4G, Wifi

[server_remote]

[filter_remote]

https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/hostsVN-quantumult-exceptions-rule.conf, tag=🚀AikoCute🚀-EXRule, force-policy=direct, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/hostsVN-quantumult-rule.conf, tag=🚀AikoCute🚀-Rule, force-policy=Chặn Ads, enabled=true
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/hostsVN-quantumult-OTA.conf, tag=🚀AikoCute🚀-OTA, force-policy=Chặn OTA, enabled=true
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/hostsVN-quantumult-FB.conf, tag=🇻🚀AikoCute🚀-FB, force-policy=Chặn Quảng Cáo FB, enabled=true

[rewrite_remote]
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/hostsVN-quantumultX-rewrite.conf, tag=🇻🇳hostsVN, enabled=true

[server_local]
shadowsocks=127.0.0.1:8080, method=none, password=password, fast-open=false, udp-replay=false, tag=🇻🇳hostsVN

[filter_local]
ip-cidr, 10.0.0.0/8, direct
ip-cidr, 127.0.0.0/8, direct
ip-cidr, 172.16.0.0/12, direct
ip-cidr, 192.168.0.0/16, direct
ip-cidr, 224.0.0.0/24, direct
final, End

[rewrite_local]
(^https?:\/\/.+\.googlevideo\.com\/.+)(&ctier=[A-Z])(&.+) url 302 $1$3

[mitm]
passphrase = 038B66B1
p12 = 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
skip_validating_cert = true
force_sni_domain_name = true
