# 戏曲小程序接口文档

1. 首页轮播图接口

   **/api/home/slides/id/1**

   返回值 一组幻灯片

2. 戏曲分类接口

   **/api/opera/cate**

   返回值

   所有分类

3. 名家接口

   **/api/opera/person**

   可选参数 category_id 获取某个剧种下的名家列表

   默认返回值

   所有名家

4. 戏曲搜索接口

   **/api/opera/search**

   参数 keyword 【不能为空】

   可以是名家姓名、戏曲名称

5. 分剧种获取视频列表接口

   **/api/opera/operas/cate/:category_id**

   参数 

   order=-post_hits（按点击量降序） -create_time（按创建时间降序）

   page 分页查询 如2,3

   limit 限制条数 当此参数存在时，page无效

   返回值 视频列表

6. 分名家获取视频列表接口

   **/api/opera/person/operas?id=5**

   参数

   id【即名家id】

7. 获取视频列表接口

   **/api/opera/operas**

   参数 

   order=-post_hits（按点击量降序） -create_time（按创建时间降序）

   page 分页查询 如2,3

   limit 限制条数 当此参数存在时，page无效

   返回值 视频列表

8. 获取某个视频接口

   **/api/opera/operas/read/:id**

   参数 id

   返回值 视频详情

9. 某个戏曲所有评论接口

   **/api/user/opera_comments**

   参数 

   object_id =32（戏曲id）

   table_name=opera_post（关联戏曲的表名）

10. 添加评论 ~~删除评论~~

   **/api/user/opera_comments**

   post

   参数

   object_id （资讯id）
   table_name （portal_post）
   url （当前资讯的url）
   content （评论内容）

11. 获取收藏列表【喜欢】

    **/api/user/opera_favorites/my**

    参数

    table_name （opera_post）

12. 戏曲收藏

   **/api/user/opera_favorites**

   post

   参数

   object_id（戏曲id）

   table_name（戏曲所在表 opera_post）

   url 网址

   title 标题

   description 描述

13. 戏曲取消收藏

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

14. 资讯分类接口

    **/api/portal/cate**

    返回值 资讯分类

15. 资讯列表接口

    **/api/portal/articles**

    参数 order=-post_hits（按点击量降序） -create_time（按创建时间降序）

    page 分页查询 如2,3

    limit 限制条数 当此参数存在时，page无效

    category_id 分类id，如8

    返回值 资讯列表

16. 按分类获取资讯列表

    **/api/portal/articles/cate/:category_id**

    参数 order=-post_hits（按点击量降序） -create_time（按创建时间降序）

    page 分页查询 如2,3

    limit 限制条数 当此参数存在时，page无效

    category_id 分类id，如8

    返回值 资讯列表

17. 资讯详情接口

   **/api/portal/articles/read/:id**

   返回值 资讯详情

18. 某条资讯所有评论接口

   **/api/user/comments**

   参数 

   object_id =32（资讯id）

   table_name=portal_post（关联资讯的表名）

19. 增加资讯评论

    **/api/user/comments**

    post

    参数

    object_id （资讯id）
    table_name （portal_post）
    url （当前资讯的url）
    content （评论内容）

20. ~~观看历史接口~~

    ~~/history~~

    ~~参数 user_id~~

    ~~返回值 观看历史列表~~

21. ~~用户信息接口~~

    ~~/user~~

    ~~参数 openid nickname sex language city provice country headimgurl phone[可选]~~

22. 手机验证码接口

    **/api/user/sms?username=13772514189**