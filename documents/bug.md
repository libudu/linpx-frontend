### 开发人员

| 名称       | 工作描述         |
| ---------- | ---------------- |
| 林彼丢     | 主策划，主程序   |
| 安卓       | UI设计           |
| 可可虎     | 上面两位的好朋友 |
| 鱼市街群员 | 测试             |
|            |                  |



### 技术栈

| 技术类型   | 技术描述             |
| ---------- | -------------------- |
| 后端程序   | Python-Django        |
| 后端服务器 | heroku虚拟主机免费版 |
| 前端框架   | uni-app              |
|            |                      |



### 可能出现的重大风险

| 描述                 | 应对措施                                                     |
| -------------------- | ------------------------------------------------------------ |
| 举报                 | 开源、免费、无偿、自愿捐赠，本体不出现任何违反法律法规内容   |
| 作者认为侵权         | 加强作品来源提示，提前打招呼，全部来自网络公开资源           |
| 服务器配额耗尽、崩溃 | 小规模测试，提前标明，后期更换服务器                         |
| 后端pixiv账号封禁    | 1、更换为pixiv小号；2、找找有没有更好的pixiv数据接口；3、引入多账号机制 |
| 累了                 | 那不做了（雾                                                 |
|                      |                                                              |



### bug记录表

| bug描述                                                  |
| -------------------------------------------------------- |
| 快速连续收藏多个未缓存内容时，会中断之前的下载、收藏过程 |
| 按作品搜索使用的是按作者搜索的接口                       |
|                                                          |



### Todo List

##### 描述性Todo

| 描述                                       | 领域                 | 完成 |
| ------------------------------------------ | -------------------- | ---- |
| 【版权信息】原作者名称、链接、作品发布时间 | 前端页面novel_detail |      |
| 【使用说明】解决问题、软件功能、备注提示   | 前端新建intro页面    |      |
|                                            |                      |      |
|                                            |                      |      |

##### 功能性Todo

| 描述                                                         | 领域                   | 完成 |
| ------------------------------------------------------------ | ---------------------- | ---- |
| 自定义添加作者快捷按钮                                       | 前端页面search         |      |
| 【收藏夹】新建收藏夹、将小说自由添加到收藏夹中               | 前端页面novels         |      |
| 【热更新】从服务器获取最新版本号数据，与本地数据对比         | 全局                   |      |
| 【本地添加】允许用户从本地或手动创建小说                     | 前端页面novels         |      |
| 【微博、b站添加】允许用户从微博、b站添加小说，或搜索作者作品 | 前端页面search、novels |      |
|                                                              |                        |      |

##### 展示性Todo

| 描述                                       | 领域                 | 完成 |
| ------------------------------------------ | -------------------- | ---- |
| 找安卓重置UI                               | 全局                 |      |
| 软件图标、软件名称                         | 全局                 |      |
| 允许用户自由调整小说详情的字体、间距、边距 | 前端页面novel_detail |      |
| 调整小说封面图样式，能够点击后放大查看     | 前端页面novel_detail |      |
| 【动画】给页面加载、组件增删加入简单动画   | 全局                 |      |
|                                            |                      |      |

##### 运营性Todo

| 描述                                                   | 完成 |
| ------------------------------------------------------ | ---- |
| 【演示视频】演示软件的使用方法                         |      |
| 【微博】发微博文字描述软件功能、下载渠道、附上演示视频 |      |
| 【QQ群】                                               |      |
| 【分享功能】                                           |      |
|                                                        |      |



### 前端文档

##### 开源信息

开源仓库地址：计划开源，暂未开源

##### 页面概览

这里的页面名称对应前端uni-app项目汇总pages目录下的页面

| 页面名称      | 页面内容                                                     |
| ------------- | ------------------------------------------------------------ |
| launch        | 【启动页面】显示logo、应用名                                 |
| novels        | 【主页面】用于查看本地小说，包括本地收藏、最近阅读，以及搜索预设的快捷入口 |
| search        | 【主搜索页面】用于搜索不同平台下的作品或作者，提供预设项     |
| search_novels | 【搜索结果】搜索某个作者，呈现出的所有小说概述内容           |
| novel_detail  | 【小说阅读】查看某个小说的具体内容，包括封面图               |
|               |                                                              |

##### 本地缓存

| 接口名称  | 接口描述 |
| --------- | -------- |
| pnXXXXX   |          |
| favNovels |          |
|           |          |

##### 非后端网络接口

pixiv相关的很多信息需要科学上网，故必须通过后端接口

但是对于国内网站，以及pixiv中没有被墙的获取图片的接口，是直接通过前端网络请求访问的

| 平台     | 内容描述         | 网址                                                    | 备注                                         |
| -------- | ---------------- | ------------------------------------------------------- | -------------------------------------------- |
| pixiv    | 小说封面图片     | 小说详情的coverUrl字段                                  | 请求头Referer必须为https://pixiv.net/        |
| bilibili | 获取用户全部文章 | https://api.bilibili.com/x/space/article?mid=【用户id】 | 请求头Referer必须为https://www.bilibili.com/ |
| bilibili | 获取特定文章内容 |                                                         |                                              |
| 微博     |                  |                                                         |                                              |
| 微博     |                  |                                                         |                                              |
|          |                  |                                                         |                                              |



### 后端文档

##### 后端地址

https://linpicio.herokuapp.com/furryreader/

##### 后端接口

| 接口名称     | 参数            | 返回                   |
| ------------ | --------------- | ---------------------- |
| user_novels  | id：pixiv作者id | 该作者的第一页小说概览 |
| novel_detail | id：pixiv作品id | 该作品的详细信息       |
|              |                 |                        |



### 运营文档



### 捐赠列表

| 用户名   | 账号        | 金额 | 时间      | 形式     |
| -------- | ----------- | ---- | --------- | -------- |
| 神采飞扬 | QQ437175144 | 20   | 2020.11.8 | QQ群红包 |
|          |             |      |           |          |
|          |             |      |           |          |