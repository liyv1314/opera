# 戏曲小程序接口文档

1. ~~轮播图接口~~

   ~~/slide~~

   ~~返回值 标题、链接地址、图片~~

2. 戏曲分类接口

   **/api/opera/categories**

   返回值

   所有分类

3. 分剧种获取视频列表接口

   **opera/operas/cate/:category_id**

   参数 cate_id num is_tuijian rows pages

   返回值 视频列表

4. ~~分名家获取视频列表接口~~

   ~~参数 person_id~~

5. 获取视频接口

   **opera/operas/read/:id**

   参数 id

   返回值 视频详情

6. ~~评论接口 添加评论 删除评论~~

   ~~/commet~~

   ~~参数 user_id video_id msg~~

   ~~/delCommet~~

   ~~参数 user_id msg_id~~

7. ~~资讯分类接口~~

   ~~/infoCate~~

   ~~返回值 资讯分类~~

8. ~~资讯列表接口~~

   ~~/infoList~~

   ~~返回值 资讯列表~~

9. ~~资讯详情接口~~

   ~~/info~~

   ~~返回值 资讯详情~~

10. ~~资讯评论接口~~

  ~~/infoCommet~~

  ~~参数 user_id info_id msg~~

11. ~~观看历史接口~~

    ~~/history~~

    ~~参数 user_id~~

    ~~返回值 观看历史列表~~

12. ~~用户信息接口~~

    ~~/user~~

    ~~参数 openid nickname sex language city provice country headimgurl phone[可选]~~