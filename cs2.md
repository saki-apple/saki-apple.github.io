# 1.签到题
关注公众号 凌日网络与信息安全团队，向公众号发送 lrtctf-final 即可获取本题 Flag
lrtctf{W31c0m3_70_lrtctf2026_final_h4v3_phun!}
---
# 2.in girl
直接解压发现需要密码，但没有任何密码信息，判断可能是伪加密，通过winhex打开girl.png
![winhex打开girl.png](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7BA76ED5FB-EE28-43E8-90A5-4C4CD676A8A3%7D.png?raw=true)

搜索得到
![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7B40128588-66C9-4848-A65C-A70134CD7EF8%7D.png?raw=true)

发现50 4B 01 02附件是09 00，是伪加密的特征，于是将它修改为00 00
重新打开girl.png,发现只是个图片没有额外信息

![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7BA5EDF91C-F4EF-4F62-9260-798DA6E686D1%7D.png?raw=true)

