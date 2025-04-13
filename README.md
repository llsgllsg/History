# AlistWebDAV
主页市场OSS-自动化部署参考文件
管理员： PCL2 Homepage Plaza Official  @JingHai-Lingyun 或 @Joker2184

# 基于Github Actions的Alist全量同步方法

由`push`/`pull_request` 事件自动触发

参考库：https://github.com/Joker2184/UpdateHomepage

> [!IMPORTANT]
> 配置
> 
>在需要同步OSS的库 在根目录创建一个.github/workflows文件夹用于激活Github Actions
>
> 把Sync-to-Alist-via-WebDAV.yml丢进.github/workflows
>
>然后在库 Settings/Secrets/Actions/Repository secrets 配置以下内容
>
>${{ secrets.WEBDAV_HOST }} OSS域名：这个->pclhomeplazaoss.lingyunawa.top
>
>${{ secrets.WEBDAV_PORT }} OSS端口[填内部访问端口 通常指的是用于上传文件的端口为保密添加为secrets 对外请使用26994]
>
>${{ secrets.ALIST_USERNAME }}  OSSID[凌云发你的ID 一般为GxxxxxID 若新人加入请私聊凌云]
>
>${{ secrets.ALIST_PASSWORD }}  OSS密码[凌云发你的密码 一般为GxxxxxID@Alist 若新人加入请私聊凌云]
>
> Name填入WEBDAV_HOST
> Secret就填入pclhomeplazaoss.lingyunawa.top
> 然后保存
> 再创建新的Secret
> 按上述填完
> 
>![QQ20241116-222726](https://github.com/user-attachments/assets/e9ed6652-8b74-4352-9440-7d8ec3f84f8f)
> 
>需要联系 @JingHai-Lingyun 或 @Joker2184 开通 OSS Webdav 使用（默认不开通）


> [!CAUTION]
> 其他
> 
> 请配置一个Reload.md用于重载Actions
> 
> 有时候出错了 可以用reload重载推送（）
