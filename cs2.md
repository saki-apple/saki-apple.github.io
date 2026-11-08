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


然后通过exiftool打开girl.png


![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7B219F580A-6CFA-4509-82C5-9AE90EE648F5%7D.png?raw=true)

发现它其实是jpg文件，修改文件后缀名后，再次用winhex打开，查找"FF09"，发现jpg文件后还有一大串字符

![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7B9AA0C4E7-49E8-4A70-A2AF-45DC6F5403F0%7D.png?raw=true)

发现"89504E..."刚好是png的固定文件头，然后选中89到末尾，然后创建新文件，将文件扩展名改为.png，打开


![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7B4F44E79E-9F1B-4728-B918-50E0A7B26814%7D.png?raw=true)

扫描二维码的flag
lrtctf{139e1603741c4ffb4a88a7776d79ab6f}
---

# 口算

下载题目附件到本地，打开

![](https://github.com/saki-apple/saki-apple.github.io/blob/main/%7BAD458EF9-98D4-4125-B689-640F82377587%7D.png?raw=true)

题目让解出m，于是m=65
lrtctf{65}

