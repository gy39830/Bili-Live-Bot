# B站直播答谢姬

## 配置

文件`conf/user.toml`

1. 填入账号密码
2. 修改`manage_room=[直播间长ID]`
3. 定时循环发送的公告内容 `alerts = ["广告1", "广告2"]``
4. 循环时间间隔 `alert_second = 300`, 当开播时才会发送，单位是秒
5. 礼物连送等待 `gift_comb_delay = 3`, 避免连送导致多条感谢
6. 送礼感谢格式 `gift_thx_format = "感谢{username}投喂的{giftname}x{num}"` 大括号里面的是替换变量
6.1 银瓜子感谢格式 `silver_gift_thx_format = "感谢{username}投喂的{giftname}x{num}"` 大括号里面的是替换变量
6.2 银瓜子感谢格式 `gold_gift_thx_format = "感谢{username}投喂的{giftname}x{num}"` 大括号里面的是替换变量
7. 上船感谢格式 `guard_thx_format = "感谢{username}投喂的{giftname}x{num}`"
8. 关注感谢格式 `focus_thx_format = "谢谢{username}的关注"`
9. 粉丝牌子升级(只能统计前50)`medal_update_format = "恭喜{username}的牌牌升到LV{new_level}!"`
10. 感谢礼物是否只在开播时开启`only_live_thx = false`
11. 新关注检查周期 `fans_check_delay = 30`
12. 粉丝牌子检查周期`medal_update_check_delay = 60`
13. 支持[[users.reply]]添加自动回复，[[users.ban]]添加自动禁言
14. 增加了一个玩法，金瓜子统计weight/银瓜子统计height

## 代码中默认配置

文件 `danmu/bili_danmu_giftthx.py`

1. 默认弹幕长度为30，修改字段为`default_length=30` (一般用户30级就有30长度了，因此不在配置中提供)


## 赞助和协议

1. 新功能一律提issue
2. 允许使用本代码在淘宝等商家提供代挂服务
3. 接受赞助：请直接在 https://live.bilibili.com/8478563 上船
