# 戏曲小程序接口文档

1. 轮播图接口

   /slide

   返回值 标题、链接地址、图片

2. 戏曲分类接口

   /cate

   返回值

   所有分类

3. 分剧种获取视频列表接口

   /videoList

   参数 cate_id num is_tuijian rows pages

   返回值 视频列表

4. 获取视频接口

   /video

   参数 id

   返回值 视频详情

5. 评论接口 添加评论 删除评论

   /commet

   参数 user_id video_id msg

   /delCommet

   参数 user_id msg_id

6. 资讯分类接口

   /infoCate

   返回值 资讯分类

7. 资讯列表接口

   /infoList

   返回值 资讯列表

8. 资讯详情接口

   /info

   返回值 资讯详情

9. 资讯评论接口

   /infoCommet

   参数 user_id info_id msg

10. 观看历史接口

    /history

    参数 user_id

    返回值 观看历史列表

11. 用户信息接口

    还要其他什么信息？