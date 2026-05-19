# Wi-Fi Calling

## 流程
```
# ==========================================
# 🟢 阶段 1: OS级环境伪装与通用配置 (Geo-Spoofing & Provisioning)
# ==========================================
- DOMAIN-SUFFIX,gspe1-ssl.ls.apple.com
- DOMAIN-SUFFIX,entitlement.apple.com

# ==========================================
# 🟢 阶段 2: 3GPP 核心网关自动发现 (Service Discovery)
# ==========================================
- DOMAIN-KEYWORD,mcc234
- DOMAIN-SUFFIX,3gppnetwork.org

# ==========================================
# 🔴 阶段 3: 各运营商定制化路由 (Media Plane & Entitlement)
# ==========================================
# Vodafone UK Group
# EE / BT Group
# O2 UK (Telefonica) Group
```

## 概念

>Mobile Country Codes (MCC) and Mobile Network Codes (MNC): https://www.mcc-mnc.com/


### 域名
- 运营商特定的EPDG服务器域名：epdg.epc.mnc260.mcc310.pub.3gppnetwork.org
- IMS服务器：ims.epc.mnc260.mcc310.pub.3gppnetwork.org
- 运营商APN设置相关域名：fast.t-mobile.com
- 通用VoIP和通信服务域名：sip.att.net、vzw.voip.verizonwireless.com

苹果定位的域名
```
DOMAIN,gspe1-ssl.ls.apple.com
```

全球运营商走 Wi-Fi Calling 通用的域名，请将mnc000.mcc000替换成正确的编号
可在 https://mcc-mnc-list.com/list 查询
通用的部分，直接对比后缀域名

## 支持清单
### 北美
#### 美国
- T-Mobile
- AT&T
- Verizon

### 中国
#### 香港

### 欧洲
#### 英国

- https://github.com/darkli/research/blob/main/rules/rules_set/uk_vowifi.yaml


## 参考
- iniwex5/tools https://github.com/iniwex5/tools
- https://github.com/lilith-rong/PrivateClashRules
- https://github.com/aoch1/clash-rule