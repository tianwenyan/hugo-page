---
date: "2019-05-23"
title: "接收第三方微博登陆"
---

申请成为新浪微博开发者流程

新建应用

获取appid和app秘钥

具体流程

新浪微博拼接登录代码

```
#新浪微博登录地址组合返回（第一步）
class SinaFirstHandler(BaseHandler):

    def get(self,*args,**kwargs):

        #微博接口地址
        weibo_auth_url = "https://api.weibo.com/oauth2/authorize"
        #回调网址
        redirect_url = "http://127.0.0.1:8000/md_admin/weibo"
        #应用id
        client_id = "2636039333"
        #组合url
        auth_url = weibo_auth_url + "?client_id={client_id}&redirect_uri={re_url}".format(client_id=client_id,
                                                                                        re_url=redirect_url)
        self.write(auth_url)
```