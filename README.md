# Config
Bitbucket with proxy is still very slow also said in https://community.atlassian.com/forums/Bitbucket-questions/Why-is-BitBucket-slow/qaq-p/834812...
- See https://johnshall.github.io/Shadowrocket-ADBlock-Rules-Forever/lazy.conf except for
  - `SCRIPT` see https://raw.githubusercontent.com/mymoonyue/Shadowrocket/refs/heads/master/mianliu.conf which just does something using js etc for some domain etc at least for cron.
    - LengZz (**no ad blocking** & use no `RULE-SET` etc) https://raw.githubusercontent.com/lengzziosofficialscript/scriptvipshadowrocket/main/LengZz.configuration → https://raw.githubusercontent.com/lengzziosofficialscript/scriptvipshadowrocket/main/KinemasterScript.json
    I tested with one Kinemaster account but it has no annual subscription… (Needs network capturing https://developer.apple.com/documentation/network/recording-a-packet-trace. For linux we use https://github.com/gh2o/rvi_capture)
      - `[MITM]` https://www.ipway.com/blog/mastering-proxies-with-shadowrocket/Probably debug on Xcode?
      - So the above two **can’t be used well temporarily** for me.
  - Module https://github.com/BlingCc233/MITM_modules?tab=readme-ov-file is similar to config as App description says
- Comparison
  - https://raw.githubusercontent.com/mymoonyue/Shadowrocket/refs/heads/master/mianliu.conf
    - `REJECT` 730
    - Proxy and Direct are all based on **maintained** `RULE-SET` or `DOMAIN-SET` .
  - Here I just choose https://raw.githubusercontent.com/Tartarus2014/Shadowrocket-Script/main/Shadowrocket.conf which uses all from `RULE-SET` or `DOMAIN-SET` for `REJECT` etc.
    - https://raw.githubusercontent.com/zwf234/rules/master/Shadowrocket/qixin.conf has some `DOMAIN-SET` omitted
  - https://bitbucket.org/anom_mony/shadowrocket_conf/raw/master/sr_top500_banlist_ad.conf based on https://raw.githubusercontent.com/iSteal-it/script/main/shadowrocket.configuration always needs *manual* addition, so skipped.
# Comparison
- hiddify has no Shadowsocks support
- sing-box has no VMESS support https://sing-box.sagernet.org/manual/proxy-protocol/shadowsocks/
## Doc
- ~~Shadowrocket~~, [Kitsunebi](https://www.kitslabs.com/support/), ~~Quantumult X~~ have no official doc.
- > Potatso Lite,Potatso 2,Kitsunebi,Pesi,Pharos Pro
  https://iyideng.org/tools/best-ios-shadowrocket-quantumult-x-surge-loon-clients.html#6%E3%80%81iOS%E4%BB%A3%E7%90%86%E8%BD%AF%E4%BB%B6%E6%8E%A8%E8%8D%90
  Pesi is not found.
  Potatso Lite may be Potatso.
  Pharos Pro https://pharospro.com/ is dead.
  - https://www.blackhatworld.com/seo/best-iphone-proxy-utility-tool.1521498/ has much less good recommendations.
- Shadowrocket see that in telegram channel, https://github.com/LOWERTOP/Shadowrocket-First?tab=readme-ov-file https://github.com/XiangwanGuan/Shadowrocket?tab=readme-ov-file etc.
  - So the formerly asked question in twitter can be solved
    > I don't find one official doc on the internet. So I ask some questions here. 0. Is there one official doc saying about proxy group and different Rule settings? 1. What is ordering of the Rule application if there are 2 rules working for one ip/domain?
    - proxy group -> surge doc / https://github.com/LOWERTOP/Shadowrocket?tab=readme-ov-file#%E4%BB%A3%E7%90%86%E5%88%86%E7%BB%84 where the latter has "random" description.
    - Rule settings & ordering: see https://github.com/LOWERTOP/Shadowrocket?tab=readme-ov-file#%E8%A7%84%E5%88%99%E4%BC%98%E5%85%88%E7%BA%A7 or more details in "规则类型" in *channel*.
- Quantumult X doesn't have much doc, e.g. [1](https://github.com/search?q=repo%3Acrossutility%2FQuantumult-X+%24done+NOT+language%3AJavaScript+&type=code).
### `SCRIPT`
- https://www.notion.so/godtools/Loon-f0a98c39f5224c09b281c79837380431 from 
- **surge** https://manual.nssurge.com/scripting/common.html
  `script1 = type=http-response,pattern=^http://www.example.com/test,script-path=test.js,max-size=16384,debug=true`
  - API https://manual.nssurge.com/scripting/common.html#public-api with `$environment` etc.
- **egern** https://egernapp.com/docs/configuration/scriptings/ different formats from surge with *3 types*
  > HTTP request scripts (http_request), HTTP response scripts (http_response), and scheduled task scripts (schedule)
- loon https://nsloon.app/docs/Script/script_api/ similar to https://manual.nssurge.com/scripting/common.html but *less*
  - https://nsloon.app/docs/Script/#network-changed -> https://manual.nssurge.com/scripting/event.html
  - Also see https://www.notion.so/godtools/Loon-f0a98c39f5224c09b281c79837380431 from https://archive.blog.hly0928.com/post/talk-about-some-proxy-apps-on-ios/
- stash
  - https://stash.wiki/en/script/syntax-and-interface similar
  - same as egern with only 3 types but adds tile https://stash.wiki/en/script/syntax-and-interface
    `type: response # request / response`
- ~~potatso~~ so poor doc https://www.potatso.com/docs
- [lancex](https://github.com/hkjswong/shadowrocket-ipa/blob/master/ios%20app.png) has no cron https://shadowboat.app/lancexapp/scripting/
### URL-REGEX standard?
- https://manual.nssurge.com/rule/http.html no details
### USER-AGENT (with REGEX?)
- https://manual.nssurge.com/rule/http.html
  > Wildcard characters * and ? are supported.
### Version
- Shadowrocket `20 Apr 2025 Version 2.2.65 * Added DOMAIN-WILDCARD rule type`
  corresponds to
  - https://kb.nssurge.com/surge-knowledge-base/release-notes/surge-ios#version-5.11.0 `5.11.0 Apr 25, 2024`
    - i.e. https://kb.nssurge.com/surge-knowledge-base/release-notes/surge-mac#version-5.7.0
# History price
- https://appsliced.co/app?n=surge-3 Free
  - https://nssurge.com/buy_now
    > Surge iOS license is a personal license. You can only use it on your devices, which you own or control. You may not share your license with others.
    > which gives you all new feature updates *for free for one year after purchase*.
    - Same price
      > Up to 3 iOS devices for $49.99.
- https://appsliced.co/app?n=loon-13210 Loon (3 platforms ios ipadOS tvOS) increased $2 about each 2 years
- stash (3 platforms) increased $1 after 9 days... and $1 after 1 year.
  - Mac needs subcription https://stash.ws/macos/pricing/ where LifeTime is just similar to surge with only Stash 3 instead of all big versions...
- egern (2 platforms) increased $1 after 1 year.
- shadowrocket (3 platforms) just stays same.
- Quantumult X (3 platforms plus Mac) increased $2.
- lancex (2 platforms) goes free at the beginning many times.
## Unnecessary things
Based on the following and shadowrocket probably follows surge, shadowrocket is enough...
- tvOS can be done by router since it is much less possible that we move TV out of home.
- macOS is just Linux, so it is not necessary to use any of the above.
# TODO for shadowrocket counterpart
- https://egernapp.com/docs/example/http-traffic-sniffer# v2ray_linux_conf
