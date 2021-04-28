中青阅读
:warning:共两个远程重写脚本，[获取cookie]和[获取body]，有冲突，使用时请禁用其一，注意看教程说明！

--------
1⃣第一步：添加远程重写订阅

编辑配置文件，在[rewrite_remote]下粘贴以下代码：

# 中青cookie获取
https://raw.githubusercontent.com/erdongchanyo/Rules/main/Quantumult X/Youth/Youth_cookie.conf, tag=中青cookie获取, update-interval=86400, opt-parser=false, enabled=true

# 中青body获取
https://raw.githubusercontent.com/erdongchanyo/Rules/main/Quantumult X/Youth/Youth_Read.conf, tag=中青body获取, update-interval=86400, opt-parser=false, enabled=true
----------

2⃣第二步：添加定时任务
编辑配置文件，在[task_local]下粘贴以下代码：

# 中青签到&转盘宝箱
*/10 5-23 * * * https://raw.githubusercontent.com/Sunert/Scripts/master/Task/youth.js, tag= 中青签到&转盘宝箱, img-url=https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true

# 中青自动阅读
10 */2 * * * https://raw.githubusercontent.com/Sunert/Scripts/master/Task/Youth_Read.js, tag=中青自动阅读, img-url=https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true

# 中青浏览赚
20 5 10 * * * https://raw.githubusercontent.com/Sunert/Scripts/master/Task/youth_gain.js, tag=中青浏览赚, img-url=https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true
----------

3⃣第三步：食用方法:warning:

1：进入[重写]-[引用]
:white_check_mark: 启用「中青cookie获取」
:u7981: 禁用「中青阅读Body获取」

a：进入app-我的-任务中心
提示：获取cookie成功

b：进入app-我的-任务中心-看看赚-浏览赚-去白拿
提示：浏览赚获取开始请求成功

c：阅读文章或者视频，等待红包转圈结束
提示：获取阅读请求成功

d：继续阅读另一篇文章或视频
提示：获取阅读时长成功

手动执行一次「中青签到&转盘宝箱」
看签到是不是正常

2：进入[重写]-[引用]
:u7981: 禁用「中青cookie获取」
:white_check_mark: 启用「中青阅读Body获取」

阅读文章或视频，快速获取body
提示：获取第1个阅读请求成功

手动执行一次「中青自动阅读」
看脚本是否运行正常

3：点击更多文章或视频，获取更多的body
