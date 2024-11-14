# AlistWebDAV
主页市场OSS-自动化部署参考文件

# 基于Github Actions的Github Alist同步方法

目前可以达到 当库被推送新文件 Actions往OSS推

参考库：https://github.com/Joker2184/UpdateHomepage

配置

在需要同步OSS的库 创建一个.github/workflows文件夹用于激活Actions

然后在库 Settings/Secrets/Actions/Repository secrets 配置以下内容

${{ secrets.WEBDAV_HOST }} OSS域名 

${{ secrets.WEBDAV_PORT }} OSS端口

${{ secrets.ALIST_USERNAME }}  OSSID

${{ secrets.ALIST_PASSWORD }}  OSS密码

其中secrets配置时名称需要为secrets.后面的文字 比如说secrets.WEBDAV_HOST 那名称就是 WEBDAV_HOST 不可更改

需要联系 @JingHai-Lingyun 或 @Joker2184 开通 OSS Webdav 使用（默认不开通）

