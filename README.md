# AlistWebDAV
主页市场OSS-自动化部署参考文件

# 基于Github Actions的Github Alist同步方法

目前可以达到 当库被推送新文件 Actions往OSS推

参考库：https://github.com/Joker2184/UpdateHomepage

> [!IMPORTANT]
> 配置
> 
>在需要同步OSS的库 创建一个.github/workflows文件夹用于激活Actions
>
>然后在库 Settings/Secrets/Actions/Repository secrets 配置以下内容
>
>${{ secrets.WEBDAV_HOST }} OSS域名[这个]([pclhomeplazaoss.lingyunawa.top)
>
>${{ secrets.WEBDAV_PORT }} OSS端口[填内部访问端口]
>
>${{ secrets.ALIST_USERNAME }}  OSSID[凌云发你的ID 一般为GxxxxxD]
>
>${{ secrets.ALIST_PASSWORD }}  OSS密码[凌云发你的密码 一般为GxxxxxID@Alist]
>
>其中secrets配置时名称需要为secrets.后面的文字 比如说secrets.WEBDAV_HOST 那名称就是 WEBDAV_HOST 不可更改
> 
>![QQ20241116-222726](https://github.com/user-attachments/assets/e9ed6652-8b74-4352-9440-7d8ec3f84f8f)
> 
>需要联系 @JingHai-Lingyun 或 @Joker2184 开通 OSS Webdav 使用（默认不开通）


> [!CAUTION]
> 本配置文件是先删除目标OSS内所有文件再上传Github库文件
> 
> 请配置一个Reload.md用于重载Actions
> 
> Reload.md不会影响主页运行 但是如果配置完把文件删完替换成其他的就会了.jpg
