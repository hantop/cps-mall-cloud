# cps-mall
优惠券小程序后台，支持淘宝、拼多多、京东、唯品会、蘑菇街，采用SpringCloud微服务架构。精力有限前端仅适配了微信小程序，可根据接口自行适配PC、H5、App等平台。

##### 微信扫码预览：
![微信扫码预览](https://mall-share.oss-cn-shanghai.aliyuncs.com/share/untitled.png?x-oss-process=image/resize,h_200,w_200 "微信扫码预览")

------------


#### 项目模块功能描述：
+ api_mall: 商城模块，整合淘宝、京东、拼多多、唯品会、蘑菇街平台的SDK，抹除各个平台间的差异，提供了统一的API
+ api_user：用户模块，包含的具体内容如下：
 + 订单查询：包含自购订单、分享订单的查询。
 + 账单查询：包含用户自购、分享、锁定产生的收益账单。
 + 三级分销：提供各级用户查询、相关收益，各级佣金比例可调。
 + 信用体系：用户购买习惯良好、使用频繁、分享好友等操作则信用提升，反之信用下降，信用越高自动返现额度越大、速度越快，增强用户体验。
 + 浏览历史、收藏记录、意见反馈等功能的支持。
+ api_pay: 支付/付款模块，为项目提供支付、付款的能力。
+ api_activite: 活动模块，可按规则配置相关营销活动，如：高温补贴、看视频领红包、分享返现等。
+ api_lottery: 道具商城，可配置添加一些功能道具，如：VIP、收益翻倍卡等营销道具。
+ api_mini: 小程序功能模块，提供微信小程序平台独有的功能，小程序登录、消息推送、服务认证、生成分享海报、生成二维码等。
+ cron_service: 定时任务模块，主要服务于用户订单，定时从cps平台拉取订单。
+ wind_control: 风控模块，初衷是用于检测拦截用户的恶意操作，减少不必要的损失，现只监控了用户的API调用记录、接口延时检测等。

#### 架构简介