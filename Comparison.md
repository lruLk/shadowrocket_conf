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
# Doc
- Kitsunebi has no doc.
- Softwares with doc
  Surge doc is best and with the newest features since many others just mimic it.
  - Shadowrocket Channel
  - Quantumult X Github (although bad without `$done` etc contexts)
  - Loon, Stash, Surge, egern, LanceX (less readable IMHO https://shadowboat.app/lancexapp/?s=done) all with website docs.
  - https://iyideng.org/tools/best-ios-shadowrocket-quantumult-x-surge-loon-clients.html#6%E3%80%81iOS%E4%BB%A3%E7%90%86%E8%BD%AF%E4%BB%B6%E6%8E%A8%E8%8D%90
    - [Potatso (Lite) & Potatso 2 with useless doc](https://www.potatso.com/docs)
    - Pharos Pro homepage dead.
    - pesi un-existing
- > I don't find one official doc on the internet. So I ask some questions here. 0. Is there one official doc saying about proxy group and different Rule settings? 1. What is ordering of the Rule application if there are 2 rules working for one ip/domain?
  [proxy group](https://github.com/LOWERTOP/Shadowrocket?tab=readme-ov-file#%E4%BB%A3%E7%90%86%E5%88%86%E7%BB%84%E7%B1%BB%E5%9E%8B)
  [Rule settings](https://github.com/LOWERTOP/Shadowrocket?tab=readme-ov-file#%E8%A7%84%E5%88%99%E7%B1%BB%E5%9E%8B)
  Better see channel help with nmBot.
  [ordering](https://github.com/LOWERTOP/Shadowrocket?tab=readme-ov-file#%E8%A7%84%E5%88%99%E4%BC%98%E5%85%88%E7%BA%A7)