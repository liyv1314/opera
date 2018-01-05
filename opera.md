# 戏曲小程序接口文档

1. 首页轮播图接口

   **/api/home/slides/id/1**

   返回值 一组幻灯片

2. 首页接口

   **/api/opera/index**

   get

   参数 无

   返回值 幻灯片 分类 以及 4个戏曲

3. 戏曲分类接口

   **/api/opera/cate**

   返回值

   所有分类

4. 名家接口

   **/api/opera/person**

   可选参数 category_id 获取某个剧种下的名家列表

   默认返回值

   所有名家

5. 戏曲搜索接口

   **/api/opera/search**

   参数 keyword 【不能为空】

   可以是名家姓名、戏曲名称

6. 分剧种获取视频列表接口

   **/api/opera/operas/cate**

   参数 

   category_id 分类id

   order=-post_hits（按点击量降序） -create_time（按创建时间降序）

   page 分页查询 如2,3

   limit 限制条数 当此参数存在时，page无效

   返回值 视频列表

7. 分名家获取视频列表接口

   **/api/opera/person/operas?id=5**

   参数

   id【即名家id】

8. 获取视频列表接口

   **/api/opera/operas**

   参数 

   order=-post_hits（按点击量降序） -create_time（按创建时间降序）

   page 分页查询 如2,3

   limit 限制条数 当此参数存在时，page无效

   返回值 视频列表

9. 获取某个视频接口

   **/api/opera/operas/read/:id**

   参数 id

   返回值 视频详情

10. 某个戏曲所有评论接口

   **/api/user/opera_comments**

   参数 

   object_id =32（戏曲id）

   table_name=opera_post（关联戏曲的表名）

11. 添加评论 ~~删除评论~~

   **/api/user/opera_comments**

   post

   参数

   object_id （资讯id）
   table_name （portal_post）
   url （当前资讯的url）
   content （评论内容）

12. 获取收藏列表【喜欢】

    **/api/user/opera_favorites/my**

    参数

    table_name （opera_post）

13. 戏曲收藏

   **/api/user/opera_favorites**

   post

   参数

   object_id（戏曲id）

   table_name（戏曲所在表 opera_post）

   title 标题

   description 描述

   thumbnail 缩略图

14. 戏曲取消收藏

    **/api/user/opera_favorites/:id**

    delete

    示例：

    > api.request({
    >
    > ​          url: 'https://op.chaosii.xin/api/user/opera_favorites/6',
    >
    > ​          method: 'DELETE',
    >
    > ​          data: {
    >
    > ​          },
    >
    > ​          success: data => {
    >
    > ​            console.log(data)
    >
    > ​          }
    >
    > ​        });

15. 资讯分类接口

    **/api/portal/cate**

    返回值 资讯分类

16. 资讯列表接口

    **/api/portal/articles**

    参数 order=-post_hits（按点击量降序） -create_time（按创建时间降序）

    page 分页查询 如2,3

    limit 限制条数 当此参数存在时，page无效

    category_id 分类id，如8

    返回值 资讯列表

17. 按分类获取资讯列表

    **/api/portal/articles/cate/:category_id**

    参数 order=-post_hits（按点击量降序） -create_time（按创建时间降序）

    page 分页查询 如2,3

    limit 限制条数 当此参数存在时，page无效

    category_id 分类id，如8

    返回值 资讯列表

18. 资讯详情接口

   **/api/portal/articles/read/:id**

   返回值 资讯详情

19. 某条资讯所有评论接口

   **/api/user/comments**

   参数 

   object_id =32（资讯id）

   table_name=portal_post（关联资讯的表名）

20. 增加资讯评论

    **/api/user/comments**

    post

    参数

    object_id （资讯id）
    table_name （portal_post）
    url （当前资讯的url）
    content （评论内容）

21. 观看历史接口

    **/user/history**

    返回值 观看历史列表

22. 用户注册登录接口

    **/api/wxapp/public/login**

    参考api.js里封装的登录方法

    > wx.login()
    >
    > loginRes: 
    >
    > {errMsg: "login:ok", code: "0112GjsQ1pIXY81NUIqQ1QnjsQ12Gjst"}
    >
    > wx.getUserInfo() 
    >
    > res:
    >
    > {"errMsg":"getUserInfo:ok","rawData":"{\"nickName\":\"李昱\",\"gender\":1,\"language\":\"zh_CN\",\"city\":\"Weinan\",\"province\":\"Shaanxi\",\"country\":\"CN\",\"avatarUrl\":\"https://wx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTLHZpXkghnf0HdzHUqdQYpNL6IjNiax9Ar2pBW4sGkevqR5C1yvicQxJHXujPcOA349HYPpb6o6kb0w/0\"}","userInfo":{"nickName":"李昱","gender":1,"language":"zh_CN","city":"Weinan","province":"Shaanxi","country":"CN","avatarUrl":"https://wx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTLHZpXkghnf0HdzHUqdQYpNL6IjNiax9Ar2pBW4sGkevqR5C1yvicQxJHXujPcOA349HYPpb6o6kb0w/0"},"signature":"4a591043b462ee4ab3d22e4e83f6c6664fee161e","encryptedData":"Equ+LmDmBesMClq/mxsI9XUqjt4lsr+joKPI4k81QiNVKamnFQMEBvMfhjb7pSVyTO6GGvh+i+UQRAXv+zLYghl1c7Fo8O8XWdVzpsE8MsGAr+SMq8ePWG8XeYvo1Wl9Cg3cO4Tq4WflTdhfqcGpBMe3ztZFBt7fT7qZjvblZBMNFH6ZZkUuudKxVP1KZRKbnreI3bQ+xk6s1BkLfh0Re3uD4vr88F0nyTWXkAwLzx+2l81fHf6G1y2HhwqRQwmSJyLXvv3GX/Oj55Xmk+0S+T7gl5MZ5pVkWTi3nJIHDtQuPIZnsQk6FYSTCPWY7yQkGRdK/n3X/xsG+2BqNwQLoio1a2pv8LSeLUylyCfVV6ld0GVzhqseNj3hj7uWzkWpG6VPry0XfInVSv/utwBJTvREk+8ClqC62fI053UiD3JimKlPeUlPfRFRmEXjyi3tv2wP5Yqx5/4b9cAb8h60DA==","iv":"1Cykswu+WuJhXRJ6vem4CQ=="}
    >
    > 参数：
    >
    > ​    code: loginRes.code,
    >
    > ​    encrypted_data: res.encryptedData,
    >
    > ​    iv: res.iv,
    >
    > ​    raw_data: res.rawData,
    >
    > ​    signature: res.signature
    >
    > 返回值:
    >
    > ​    token openid userId
    >
    > ​    注意保存这三个值
    >
    > ​    userId openid备用
    >
    > ​    token在api.request()方法中用到，可详细查看api.request()

23. 手机验证码接口

    **/api/user/sms?username=13772514189**

24. 手机绑定接口

    /api/user/bind

    参数

    mobile

    verification_code