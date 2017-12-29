# 戏曲小程序接口文档

1. 首页轮播图接口

   **/api/home/slides/id/1**

   返回值 一组幻灯片

2. 戏曲分类接口

   **/api/opera/cate**

   返回值

   所有分类

3. 分剧种获取视频列表接口

   **/api/opera/operas/cate/:category_id**

   返回值 视频列表

4. ~~分名家获取视频列表接口~~

   ~~参数 person_id~~

5. 获取视频列表接口

   **/api/opera/operas**

   返回值 视频列表

6. 获取视频接口

   **/api/opera/operas/read/:id**

   参数 id

   返回值 视频详情

7. ~~评论接口 添加评论 删除评论~~

   ~~/commet~~

   ~~参数 user_id video_id msg~~

   ~~/delCommet~~

   ~~参数 user_id msg_id~~

8. 资讯分类接口

   **/api/portal/cate**

   返回值 资讯分类

9. 资讯列表接口

   **/api/portal/articles**

   返回值 资讯列表

10. 资讯详情接口

   **/api/portal/articles/read/:id**

   返回值 资讯详情

11. ~~资讯评论接口~~

   ~~/infoCommet~~

   ~~参数 user_id info_id msg~~

12. ~~观看历史接口~~

    ~~/history~~

    ~~参数 user_id~~

    ~~返回值 观看历史列表~~

13. ~~用户信息接口~~

    ~~/user~~

    ~~参数 openid nickname sex language city provice country headimgurl phone[可选]~~