## 使用教程

【只拉 中青看点库】

    ql repo https://github.com/Yiov/wool.git "zq_"




## 2022-1-4更新


### 中青看点极速版 快应用 zqkdFast_read.js

cron：25 8-22 * * * 

说明：仅限安卓，和APP版的应用数据是分开不互通的

入口：浏览器打开即可跳转，打不开的百度搜一下

https://user.youth.cn/h5/fastAppWeb/invite/invite_ground.html

抓get包，登录账号-领红包即可获取

https://user.youth.cn/FastApi/NewTaskSimple/getTaskList

    export zqkdFastCookie="uid=***&token=***&token_id=***"


问题：有CK但是提示token失效

答：token字符里有斜杠/，请替换成%，是在不行的在请求头里复制有%的那一段

建议：改下UA，避免黑号

答：在148和164行，注意后面的不要改，截止到2.5.5，避免拉库后被覆盖，请自己复制到Scripts文件夹，再本地task



## 2022-1-3更新

关于中青低版本黑号的问题，这个也看脸

我是低版本抓了包后，强制升级了，后来也就一直用的新版本，唯一的不同是文章body，我只是把zkqd_param=换成了p=



### 中青版本V3.2.6-V3.5.5

豌豆荚普通下载

https://www.wandoujia.com/apps/7702132/history



如果被强制更新了，body要改一下，把抓到的zkqd_param=***





### 中青cookie适用

福利视频/阅读翻倍/转盘抽奖/火山爆发/每日收益/看看赚，都是通用的，抓一次即可






## 更新时间

2021-12-28


## 中青看点 新增 看看赚肥皂版 zq_kkz_fz.js

cron：随意一天一次

注意：由于这个脚本非常粗暴，直接刷完，可能会黑号！！！自行斟酌是否使用，如使用本脚本，请停用之前的看看赚zq_kkz.js

面板拉取到依赖文件CryptoJS.js后，禁用即可


打开赚赚看页面，获取url和hd

https://kd.youth.cn/webApi/Nameless/getTaskBrowse

    export zqkkzurl="https://kd.youth.cn/webApi/Nameless/getTaskBrowse?***"

请求头用链接转换：https://tooltt.com/header2json/

    export zqkkzlbhd='{"Host"***}'



打开任意新闻后，获取文章的hd和body

https://kandian.wkandian.com/v5/nameless/adlickstart.json

    export zqkkzbody="p=***"

请求头用链接转换：https://tooltt.com/header2json/

    export zqkkzrwhd='{"device-platform"***}'







## 福利视频 zq_Adv_video.js


cron：20 5 * * *

抓get包，打开app-任务-福利视频，看完即可获取

https://kandian.wkandian.com/V17/NewTask/recordNum.json?

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'






## 宝箱 zq_box.js


cron：15 22 * * *

抓post包，完成3个任务后可以开，以上首页右上角，其他用@隔开

（注意看相应是否为任务奖励）

https://kandian.wkandian.com/v5/CommonReward/toGetReward.json


    export zqboxbody='p=***@p=***'





## 阅读翻倍 zq_double.js


cron：34 5 * * 1

抓get包，打开app即可获取

https://kandian.wkandian.com/V17/NewTask/recordNum.json?

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'




## 翻倍奖励领取 zq_fbjl.js


cron：30 22 * * *

这里我只会抓签到的翻倍，也适用其他翻倍

https://kandian.wkandian.com/v5/CommonReward/toDouble/

    export zqfbjlbody=''





## 看看赚 zq_kkz.js


cron：45 9 * * *

抓get包，打开app-任务-看看赚，即可获取

https://kandian.wkandian.com/NewTask/getTaskList.josn

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'

抓POST包，一个新闻一个body，请挨个抓，其他用@隔开

https://kandian.wkandian.com/v5/nameless/adlickstart/

    export zqlookStartbody='p=***@p=***'





## 浏览赚 zq_llz.js


cron：34 6 * * *

抓POST包，进APP-任务-看看赚-浏览赚，一个新闻一个body，请挨个抓，其他用@隔开

https://kandian.wkandian.com/v5/task/browse_start.json

    export zqllzbody='p=***@p=***'







## 签到 zq_qd.js


cron：15 2 * * *

抓POST包，打开app-任务-签到，看完即可获取

（注意看相应是否为任务奖励）

https://kandian.wkandian.com/v5/CommonReward/toGetReward.json


    export zqqdbody='p=***'





## 转盘抽奖 zq_Rotary.js


cron：34 22 * * *

抓get包，打开app-任务-抽奖赚，看完即可获取

https://kandian.wkandian.com/html/rotaryTable/index.html?

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'

抽奖翻倍

https://kandian.wkandian.com/v5/RotaryTable/toTurnDouble.json




## 火山爆发 zq_share.js


cron：15 6,12,18 * * *

抓get包，打开app-赚钱-火山爆发，看完即可获取

https://kandian.wkandian.com/h5/20200612makeMoney/?

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'




## 搜索赚 zq_ssz.js

cron：35 5 * * *

抓POST包，打开app-看看赚-搜索赚，一个新闻一个body，请挨个抓，其他用@隔开

https://kandian.wkandian.com/v5/Sousuo/playStart.json

    export zqsszbody='p=***@p=***'





## 收益统计 zq_today_score.js


cron：15 23 * * *

抓get包，打开app-我的-今日金币，即可获取

https://kandian.wkandian.com/wap/user/balance?

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'





## 打卡赚 zq_wakeup.js

cron：34 5,9 * * *

进APP-我的-打卡赚

    export zq_cookie='zqkey=***&zqkey_id=***&uid=***'







## 提现 zq_withdraw.js


cron：34 10 * * *

抓POST包，打开app-我的-提现兑换，即可获取，提过的也可以，必须要有足够的金币能提，才可以抓

https://kandian.wkandian.com/v5/wechat/withdraw2.json

    export zq_withdraw='p=xxx'

    export zq_cash='10' #不填默认30，自己改





## 文章 zq_wz.js


cron：30 7,12,18 * * *

抓get包，打开app-资讯，一个新闻一个body，请挨个抓，其他用@隔开

https://kandian.wkandian.com/v5/article/info.json

    export zqwzbody='p=***@p=***'


时长必须抓，不然黑号，抓post包，打开app-资讯，看完1分钟后即可获取，一个新闻一个body，请挨个抓，其他用@隔开

https://kandian.wkandian.com/v5/user/stay.json

    export zq_timebody='p=***p=***'




## 中青听歌 zqkd_audio_pro.js

cron：30 12 * * *（一天一次即可）

CK是格式和上面是一样的，变量不一样

    export zqkdCookie='zqkey=***&zqkey_id=***&uid=***'

青龙报错没有依赖crypto-js

      docker exec -it qinglong bash -c "npm install -g crypto-js"




## 中青看点 风险查询 zqkd_risk.js


cron：30 9 */7 * *（想跑就跑一下）

CK是格式和上面是一样的，变量不一样

    export zqkdCookie='zqkey=***&zqkey_id=***&uid=***'







## 特别鸣谢:

* [@whyour](https://github.com/whyour/qinglong)「青龙」
* [@shaolin-kongfu](https://github.com/shaolin-kongfu/js_scripts/)「少林大佬」
