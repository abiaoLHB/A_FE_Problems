# 微信开发常见问题

> ### 二次分享失败问题
>> - 描述：iOS客户端第一次分享没问题，然后打开分享链接继续分享，显示签名失败
>> - 解决方案：签名的url要`encodeURIComponent`，跳转的link不用。
>> ```js
>> var url = window.location.href.split('#')[0]
>> var splitUtl = encodeURIComponent(url)
>> var linkUrl = url
>> ```