
========模板结构=======
 │─template/1/  模板1
  │  ├─info.ini  模板信息文件
  │  ├─ads   广告文件目录
  │  ├─js    js文件
  │  ├─css   css文件
  │  ├─images   图片文件
  │  └─html     模板文件目录
  │      └─art     文章模块模板目录
  │      └─comment  评论模块模板目录
  │      └─gbook    留言本模块模板目录
  │      └─index    首页模块模板目录
  │      └─label    自定义页面模块模板目录
  │      └─map      地图页模块模板目录
  │      └─public   公共页面模板目录
  │      └─rss      RSS和sitemap模板目录
  │      └─topic    专题模块模板目录
  │      └─user     用户中心模块模板目录
  │      └─vod      视频模块模板目录
  │─tempalte/2/  模板2
  │─...
  │─template/n/  模板N

========模板目录下的info.ini介绍========
里边包含了对模板文件的简单介绍，及adsdir广告文件存放目录的设置，默认广告目录为ads

========模板名称======
public/include.html    全站公共引入文件 引入js、css样式，还有系统JS变量
public/head.html       全站头部
public/foot.html       全站尾部
public/jump.html       跳转提示页模板
public/msg.html        错误提示页模板
public/paging.html     分页样式模板
public/digg.html       顶踩样式模板
public/score.html      普通评分样式模板
public/star.html       星星评分样式模板
│
comment/index.html     评论页
comment/ajax.html     评论页
gbook/index.html       留言本
gbook/report.html      报错页面
│
index/index.html     首页
│
map/rss.html    rss
map/baidu.html   百度sitemap
map/google.html  谷歌sitemap
│
topic/index.html   专题首页
topic/detail.html  专题详情页
│
art/confirm.html     确认支付积分页面
art/detail.html      文章内容页
art/detail_pwd.html      验证密码页
art/rss.html         文章内容rss
art/search.html      文章搜索页
art/type.html        文章分类页
art/show.html        文章分类筛选页
│
vod/confirm.html     确认支付积分页面
vod/copyright.html      版权提示和跳转
vod/detail.html      视频内容页
vod/detail_pwd.html      验证密码页
vod/rss.html         视频内容rss
vod/play.html        视频播放页
vod/player.html      试看页面播放页
vod/player_pwd.html      验证密码页
vod/down.html        视频下载页
vod/downer_pwd.html      验证密码页
vod/search.html      视频搜索页面
vod/type.html        视频分类页面
vod/show.html        视频分类筛选页
│
user/ajax_info.html   用户弹出层登录详情
user/ajax_login.html  用户弹出层登录界面
user/buy.html         用户中心-在线充值
user/cards.html       用户中心-充值卡记录
user/cash.html       用户中心-提现记录
user/downs.html       用户中心-下载记录
user/favs.html        用户中心-收藏记录
user/findpass.html    用户中心-找回密码
user/findpass_msg.html    用户中心-找回密码提示信息
user/foot.html        用户中心-公共底部
user/head.html        用户中心-公共头部
user/include.html     用户中心-公共引入文件
user/index.html       用户中心-首页
user/info.html        用户中心-个人详情
user/login.html       用户中心-登录页
user/orders.html      用户中心-在线充值记录
user/pay.html         用户中心-支付页
user/payment_weixin.html         用户中心-支付微信二维码
user/plays.html       用户中心-点播记录
user/popedom.html     用户中心-权限列表
user/reg.html         用户中心-注册
user/reward.html     用户中心-分销记录
user/upgrade.html     用户中心-会员升级


========全局标签=======
{$maccms.site_name}网站名称
{$maccms.site_url}网站url
{$maccms.site_wapurl} wap网站url
{$maccms.site_logo}网站logo
{$maccms.site_waplogo} wap网站logo
{$maccms.site_keywords}网站关键字
{$maccms.site_description}网站描述
{$maccms.site_icp}备案号
{$maccms.site_qq}站长qq
{$maccms.site_email}站长email
{$maccms.site_tj}统计代码；也可以用{$maccms.path}static/js/tj.js 来动态引入统计代码。
{$maccms.site_status}网站状态1开启0关闭
{$maccms.site_close_tip}网站关闭提示信息

{$maccms.path}网站目录
{$maccms.path_tpl}当前模板目录
{$maccms.date} 当前日期
{$maccms.search_hot}       热门搜索词
{$maccms.art_extend_class}       全局文章扩展分类
{$maccms.vod_extend_class}       全局视频扩展分类
{$maccms.vod_extend_state}       全局视频资源
{$maccms.vod_extend_version}       全局视频版本
{$maccms.vod_extend_area}       全局视频地区
{$maccms.vod_extend_lang}       全局视频语言
{$maccms.vod_extend_year}       全局视频年代
{$maccms.vod_extend_weekday}       全局视频更新周期
{$maccms.actor_extend_area}       全局演员地区
{$maccms.http_type}  当前url访问协议，会输出 http:// 或者 https://

如果$maccms.标签不够用，想调用其他配置项的内容，可以用$GLOBALS['config'] 来获取到
例如
{$GLOBALS['config']['site']['site_name']}
其他项：具体包含哪些属性可以调试查看下;{php} dump($GLOBALS['config']);die; {/php}

$GLOBALS['config']['site'] 站点配置
$GLOBALS['config']['app'] 预留参数配置
$GLOBALS['config']['user'] 用户配置
$GLOBALS['config']['gbook'] 留言本配置
$GLOBALS['config']['comment'] 评论配置
$GLOBALS['config']['upload'] 上传配置
$GLOBALS['config']['interface'] 站外入库配置
$GLOBALS['config']['pay'] 支付配置
$GLOBALS['config']['collect'] 采集配置
$GLOBALS['config']['api'] api配置
$GLOBALS['config']['connect'] 第三方登录配置
$GLOBALS['config']['weixin'] 微信配置
$GLOBALS['config']['view'] url浏览模式配置
$GLOBALS['config']['path'] url静态路径配置
$GLOBALS['config']['rewrite'] 路由配置
$GLOBALS['config']['weixin'] 微信配置
$GLOBALS['config']['email'] 邮件配置
$GLOBALS['config']['play'] 播放器配置
$GLOBALS['config']['urlsend'] url推送配置
$GLOBALS['config']['sms'] 短信配置
$GLOBALS['config']['extra'] 自定义参数配置

------------------下方高能------------------------------
$GLOBALS['type_id']  当前分类页ID，在（分类页，筛选页，内容页，播放页，下载页都有值）
$GLOBALS['type_pid']  当前分类页父ID，在（分类页，筛选页，内容页，播放页，下载页都有值）

{$maccms.mid}模块id，1=>'视频',2=>'文章',3=>'专题',4=>'评论',5=>'留言',6=>'用户中心',7=>'自定义页面',8=>'明星',9=>'角色'

{$maccms.aid}当前系统页面id
首页1
地图2
rss3
留言本4
评论5
用户中心6
自定义页面7


视频首页10
视频分类页11
视频分类筛选12
视频搜索13
视频详情14
视频播放15
视频下载16
视频角色17

文章首页20
文章分类21
文章分类筛选22
文章搜索23
文章详情24

专题首页30
专题搜索33
专题详情34

明星首页80
明星搜索83
明星详情84

角色首页90
角色搜索93
角色详情94
------------------------------------------------
设计首页幻灯片的时候，建议统一调用推荐值为9的数据~


=======引入模板文件=======
{include file="public/head"}


=======分类列表标签=======
order排列顺序desc倒序，asc正序
by排序依据  id,sort
start从第几条开始
num获取条数
ids指定分类parent获取一级分诶；child获取子分类；1,2,3一组指定ID；
parent父分类id
flag视频=vod文章=art
cachetime自定义缓存时间单位秒

{maccms:type num="10" order="asc" by="sort" ids="all"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:type}

嵌套标签获取一级及二级
{maccms:type ids="1,2,3,4" order="asc" by="sort" id="vo1" key="key1"}
  一级分类：{$vo1.type_name}-
  {maccms:type parent="'.$vo1['type_id'].'" order="asc" by="sort" id="vo2" key="key2"}
     二级分类{$vo2.type_name}
  {/maccms:type}
  <br>
{/maccms:type}

=======分类页独有标签=======
{$obj.parent} 如果当前访问的是二级分类，这个是一级分类对象，也同样包含以下属性，如{$obj.parent.type_id}一级分类id

{$obj.type_id}分类id
{$obj.type_name}名称
{$obj.type_en}别名
{$obj.type_sort}排序号
{$obj.type_mid}所属模块
{$obj.type_pid}上级id
{$obj.type_status}状态1开启0关闭
{$obj.type_tpl}分类页模板
{$obj.type_tpl_list}筛选页模板
{$obj.type_tpl_detail}详情页模板
{$obj.type_tpl_play}播放页模板
{$obj.type_tpl_down}下载页模板
{$obj.type_key}关键字
{$obj.type_des}描述信息
{$obj.type_title}标题
{$obj.type_extend}扩展配置json
{:mac_url_type($obj)} 分类链接

=======专题列表标签=======
order排列顺序desc倒序，asc正序
by排序依据 id, time,time_add,score,hits,hits_day,hits_week,hits_month,up,down,level,rnd
start从第几条开始
num获取条数
ids指定1,2,3一组指定ID；
timeadd添加时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
timehits点击时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
time更新时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
hitsmonth月点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsweek周点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsday日点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hits总点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
paging是否分页yes

{maccms:topic num="10" paging="no" order="asc" by="sort" ids="all"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:topic}
=======专题页独有标签=======
{$obj.topic_id}专题id
{$obj.topic_name}名称
{$obj.topic_en}别名
{$obj.topic_sub}副标
{$obj.topic_status}状态
{$obj.topic_sort}排序号
{$obj.topic_letter}首字母
{$obj.topic_color}高亮颜色
{$obj.topic_tpl}模板文件
{$obj.topic_type}扩展分类
{$obj.topic_pic}图片
{$obj.topic_pic_thumb}缩略图
{$obj.topic_pic_slide}幻灯图
{$obj.topic_key}seo关键字
{$obj.topic_des}seo描述
{$obj.topic_title}seo标题
{$obj.topic_blurb}简介
{$obj.topic_remarks}备注
{$obj.topic_level}推荐值
{$obj.topic_up}顶数
{$obj.topic_down}踩数
{$obj.topic_score}平均分
{$obj.topic_score_all}总评分
{$obj.topic_score_num}总评次
{$obj.topic_hits}总点击
{$obj.topic_hits_day}日点击
{$obj.topic_hits_week}周点击
{$obj.topic_hits_month}月点击
{$obj.topic_time}更新时间
{$obj.topic_time_add}添加时间
{$obj.topic_content}详细介绍
{$obj.topic_extend}扩展配置json
{$obj.topic_rel_vod|explode=',',###|count} 专题包含视频数量
{$obj.topic_rel_art|explode=',',###|count} 专题包含文章数量
{:mac_url_topic_detail($obj)} 专题详情页链接
{:mac_url_topic_index()}  专题首页链接

=======视频列表标签=======
order排列顺序desc倒序，asc正序
by排序依据 id,time,time_add,score,hits,hits_day,hits_week,hits_month,up,down,level,rnd
start从第几条开始
num获取条数
ids指定1,2,3一组ID；
not不抱含id 多个逗号链接
type指定获取分类数据 all所有；1,2,3指定；
class指定某扩展分类 支持多个 动作,喜剧
tag指定tag 支持多个  aaa,xxx
level指定推荐值 支持多个  1,2
area指定地区 支持多个  大陆,香港
lang指定语言 支持多个  国语,粤语
year指定年代 支持多个 2002,2003
state资源类别 支持多个 高清版,剧场版,抢先版
version资源版本 支持多个 正片,预告片
weekday更新周期 支持多个  一,二,三
rel指定关联数据 1,2,3 或 变形金刚
timeadd添加时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
timehits点击时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
time更新时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
hitsmonth月点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsweek周点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsday日点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hits总点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
paging是否分页yes
pageurl分页地址
cachetime自定义缓存时间单位秒


{maccms:vod num="10" paging="no" type="all" order="asc" by="sort"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:vod}
=======视频内容页独有标签=======
{$obj.vod_id} 视频id
{$obj.type_id} 分类id
{$obj.type_id_1} 一级分类id
{$obj.type} 分类对象，二级属性可参考分类属性
{$obj.type.type_name} 分类名
{$obj.type.type_en} 分类拼音
{$obj.type_1} 一级分类对象，二级属性可参考分类属性
{$obj.type_1.type_name} 一级分类名
{$obj.type_1.type_en} 一级分类拼音
{$obj.group_id} 用户组id
{$obj.vod_name} 视频名
{$obj.vod_sub} 副标题
{$obj.vod_en} 别名
{$obj.vod_status} 状态0未审1已审
{$obj.vod_letter} 首字母
{$obj.vod_color} 颜色
{$obj.vod_tag} tags
{$obj.vod_class} 扩展分类
{$obj.vod_pic} 图片
{$obj.vod_pic_thumb} 缩略图
{$obj.vod_pic_slide} 幻灯图
{$obj.vod_actor} 主演
{$obj.vod_director} 导演
{$obj.vod_writer}编剧
{$obj.vod_behind}幕后
{$obj.vod_blurb} 简介
{$obj.vod_remarks} 备注
{$obj.vod_pubdate}上映日期
{$obj.vod_total} 总集数
{$obj.vod_serial} 连载数
{$obj.vod_tv} 上映电视台
{$obj.vod_weekday} 节目周期
{$obj.vod_area} 地区
{$obj.vod_lang} 语言
{$obj.vod_year} 年代
{$obj.vod_version} 版本-dvd,hd,720p
{$obj.vod_state} 资源类别-正片,预告片,花絮
{$obj.vod_author} 编辑人员
{$obj.vod_jumpurl} 跳转url
{$obj.vod_tpl} 独立模板
{$obj.vod_tpl_play} 独立播放页模板
{$obj.vod_tpl_down} 独立下载页模板
{$obj.vod_isend} 是否完结
{$obj.vod_lock} 锁定1
{$obj.vod_level} 推荐级别
{$obj.vod_points} 访问整个视频所需积分
{$obj.vod_points_play} 每集点播付费
{$obj.vod_points_down} 每集下载付费
{$obj.vod_hits} 总点击量
{$obj.vod_hits_day} 日点击量
{$obj.vod_hits_week} 周点击量
{$obj.vod_hits_month} 月点击量
{$obj.vod_duration} 时长
{$obj.vod_up} 顶数
{$obj.vod_down} 踩数
{$obj.vod_score} 平均分
{$obj.vod_score_all} 总评分
{$obj.vod_score_num} 评分次数
{$obj.vod_time} 更新时间
{$obj.vod_time_add} 添加时间
{$obj.vod_time_hits} 点击时间
{$obj.vod_time_make} 生成时间
{$obj.vod_trysee} 试看时长分
{$obj.vod_reurl} 来源地址
{$obj.vod_rel_vod} 关联视频ids
{$obj.vod_rel_art} 关联文章ids
{$obj.vod_content} 详细介绍
{$obj.vod_pwd} 访问内容页密码
{$obj.vod_pwd_url} 获取密码链接
{$obj.vod_pwd_play} 访问播放页密码
{$obj.vod_pwd_play_url} 获取密码链接
{$obj.vod_pwd_down} 访问下载页密码
{$obj.vod_pwd_down_url} 获取密码链接
{$obj.vod_copyright} 是否开启版权提示
{$obj.vod_play_from} 播放组
{$obj.vod_play_server} 播放服务器组
{$obj.vod_play_note} 播放备注
{$obj.vod_play_url} 播放地址
{$obj.vod_down_from} 下载租
{$obj.vod_down_server} 下载服务器组
{$obj.vod_down_note} 下载备注
{$obj.vod_down_url} 下载地址
{:mac_url_vod_detail($obj)}  视频详情页链接
{:mac_url_vod_play($obj,['sid'=>1,'nid'=>1])}   视频播放页链接
{:mac_url_vod_play($obj,'first')}   视频播放页第一条链接
{:mac_url_vod_down($obj,['sid'=>1,'nid'=>1])}   视频下载页链接
{:mac_url_vod_down($obj,'first')}   视频下载页第一条链接

=======视频播放地址和下载地址标签=======

{maccms:foreach name="obj.vod_play_list" id="vo"}
<div class="ui-box marg" id="playlist_1">
    <div class="down-title">
        <h2>{$vo.from}-在线播放</h2><span>[{$vo.player_info.tip}]</span>
    </div>
    <div class="video_list fn-clear">
        {maccms:foreach name="vo.urls" id="vo2"}
        <a href="{:mac_url_vod_play($obj,['sid'=>$vo.sid,'nid'=>$vo2.nid])}" >{$vo2.name}</a>
        {/maccms:foreach}
    </div>
</div>
{/maccms:foreach}


{maccms:foreach name="obj.vod_down_list" id="vo"}
<div class="ui-box marg" id="downlist_1">
    <div class="down-title">
        <h2>{$vo.from}-下载</h2><span>[{$vo.player_info.tip}]</span>
    </div>
    <div class="video_list fn-clear">
        {maccms:foreach name="vo.urls" id="vo2"}
        <a href="{:mac_url_vod_down($obj,['sid'=>$vo.sid,'nid'=>$vo2.nid])}" >{$vo2.name}</a>
        {/maccms:foreach}
    </div>
</div>
{/maccms:foreach}


如何在播放页或下载页只显示当前分组的地址呢？外层循环标签不变，只需要加一个判断就可以了。
{maccms:foreach name="obj.vod_play_list" id="vo"}
{if condition="$vo.sid eq $param.sid"}    ---------------------重点是这句if判断
<div class="ui-box marg" id="playlist_1">
    <div class="down-title">
        <h2>{$vo.from}-在线播放</h2><span>[{$vo.player_info.tip}]</span>
    </div>
    <div class="video_list fn-clear">
        {maccms:foreach name="vo.urls" id="vo2"}
        <a href="{:mac_url_vod_play($obj,['sid'=>$vo.sid,'nid'=>$vo2.nid])}" >{$vo2.name}</a>
        {/maccms:foreach}
    </div>
</div>
{/if}
{/maccms:foreach}


上边循环过程中，其中获取播放器详细信息的方法是
{$vo.player_info.from} 编码
{$vo.player_info.show} 名称
{$vo.player_info.des} 备注
{$vo.player_info.tip} 提示
{$vo.player_info.sort} 排序
{$vo.player_info.parse} 解析接口
{$vo.from} 播放器编码
{$vo.note} 备注
{$vo.url}  url地址
{$vo.url_count} 集数




=======视频播放页独有标签=======
{$param.sid} 当前播放组序号
{$param.nid} 当前集数序号

{$obj.player_info.link_next} 下一页地址，最后一页时此链接将当前页链接
{$obj.player_info.link_pre} 上一页地址，第一页时此链接将当前页链接

{$obj['vod_play_list'][$param['sid']]} 获取当前播放组数据
{$obj['vod_play_list'][$param['sid']]['player_info']}  播放器信息
{$obj['vod_play_list'][$param['sid']]['server_info']}  服务器组信息
{$obj['vod_play_list'][$param['sid']]['url_count']} 总集数
{$obj['vod_play_list'][$param['sid']]['urls']} 集数信息
{$obj['vod_play_list'][$param['sid']]['urls'][$param['nid']]} 当前集数信息
{$obj['vod_play_list'][$param['sid']]['urls'][$param['nid']]['name']} 当前集数名称
{$obj['vod_play_list'][$param['sid']]['urls'][$param['nid']]['url']} 当前集数url

下载页获取以上信息，请把vod_play_list改为vod_down_list，其他参数不变

{$player_data} 播放数据
{$player_js} 加载播放器
=======获取与当前视频相关联视频和关联文章数据======
<h2>与<strong>“{$obj.vod_name}”</strong>关联的视频</h2>
<ul class="img-list dis">
    {maccms:vod num="6" ids="'.$obj['vod_rel_vod'].'" order="desc" by="time"}
        <li><a href="{:mac_url_vod_detail($vo)}" title="{$vo.vod_name}"><img src="{:mac_url_img($vo.vod_pic)}" alt="{$vo.vod_name}"/><h2>{$vo.vod_name}</h2><p></p><i>{$vo.vod_version}</i><em></em></a></li>
    {/maccms:vod}
</ul>
<h2>与<strong>“{$obj.vod_name}”</strong>关联的文章</h2>
<ul class="img-list dis">
    {maccms:art num="6" ids="'.$obj['vod_rel_art'].'" order="desc" by="time"}
        <li><a href="{:mac_url_art_detail($vo)}" title="{$vo.art_name}"><img src="{:mac_url_img($vo.art_pic)}" alt="{$vo.art_name}"/><h2>{$vo.art_name}</h2><p></p><i>{$vo.vod_from}</i><em></em></a></li>
    {/maccms:art}
</ul>


版权跳转？配合后台提供的跳转url字段，在内容页播放页通用。
<script>
    {if condition="$obj.vod_jumpurl neq ''"}
        location.href='{$obj.vod_jumpurl}';
    {/if}
</script>
如果想判断每集是否跳转，可把要跳转的集数地址写成固定的格式，方便读取和操作。
比如火影忍者有10集， 第2集版权跳转，地址写为jump://baidu.com
在播放页加入代码 只跳转这一集
<script>
    {if condition="strpos($obj['vod_play_list'][$param['sid']]['urls'][$param['nid']]['url'],'jump:')!==false "}
        location.href='{$obj['vod_play_list'][$param['sid']]['urls'][$param['nid']]['url']|str_replace="jump:","http:",###}';
    {/if}
</script>






=======文章列表标签=======
order排列顺序desc倒序，asc正序
by排序依据 id,time,time_add,score,hits,hits_day,hits_week,hits_month,up,down,level,rnd
start从第几条开始
num获取条数
ids指定1,2,3一组ID；
not不抱含id 多个逗号链接
type指定获取分类数据 all所有；1,2,3指定；
class指定某扩展分类 支持多个
tag指定tag 支持多个  aaa,xxx
level指定推荐值 支持多个
rel指定关联数据 1,2,3 或 变形金刚
timeadd添加时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
timehits点击时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
time更新时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
hitsmonth月点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsweek周点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsday日点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hits总点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
paging是否分页yes
pageurl分页地址
cachetime自定义缓存时间单位秒

{maccms:art num="10" paging="no" type="all" order="asc" by="sort"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:art}
=======文章内容页独有标签=======
{$obj.art_id} 文章id
{$obj.type_id} 分类id
{$obj.type_id_1} 一级分类id
{$obj.type} 分类对象，二级属性可参考分类属性
{$obj.type.type_name} 分类名
{$obj.type.type_en} 分类拼音
{$obj.type_1} 一级分类对象，二级属性可参考分类属性
{$obj.type_1.type_name} 一级分类名
{$obj.type_1.type_en} 一级分类拼音
{$obj.group_id} 用户组id
{$obj.art_name} 标题
{$obj.art_sub} 副标题
{$obj.art_en} 别名
{$obj.art_status} 状态0未审1已审
{$obj.art_letter} 首字母
{$obj.art_color} 颜色
{$obj.art_from} 来源
{$obj.art_author} 作者
{$obj.art_tag} tags
{$obj.art_class} 扩展分类
{$obj.art_pic} 主图
{$obj.art_pic_thumb} 缩略图
{$obj.art_pic_slide} 幻灯图
{$obj.art_blurb} 简介
{$obj.art_remarks} 备注
{$obj.art_jumpurl} 跳转url
{$obj.art_tpl} 独立模板
{$obj.art_level} 推荐等级
{$obj.art_lock} 锁定
{$obj.art_up} 顶数
{$obj.art_down} 踩数
{$obj.art_hits} 总点击量
{$obj.art_hits_day} 日点击量
{$obj.art_hits_week} 周点击量
{$obj.art_hits_month} 月点击量
{$obj.art_time} 更新时间
{$obj.art_time_add} 添加时间
{$obj.art_time_hits} 点击时间
{$obj.art_time_make} 生成时间
{$obj.art_score} 平均分
{$obj.art_score_all} 总评分
{$obj.art_score_num} 评分次数
{$obj.art_rel_art} 关联文章
{$obj.art_rel_vod} 关联视频
{$obj.art_title} 页标题
{$obj.art_note} 页备注
{$obj.art_content} 页详细介绍
{$obj.art_points} 访问整个文章所需点数
{$obj.art_points_detail} 访问每一页所需点数
{$obj.art_pwd} 访问密码
{$obj.art_pwd_url} 密码获取链接
{:mac_url_art_detail($obj)}  文章详情页链接


=======获取与当前文章相关联视频和关联文章数据======
<h2>与<strong>“{$obj.art_name}”</strong>关联的视频</h2>
<ul class="img-list dis">
    {maccms:vod num="6" rel="'.$obj['art_rel_vod'].'" order="desc" by="time"}
        <li><a href="{:mac_url_vod_detail($vo)}" title="{$vo.vod_name}"><img src="{:mac_url_img($vo.vod_pic)}" alt="{$vo.vod_name}"/><h2>{$vo.vod_name}</h2><p></p><i>{$vo.vod_version}</i><em></em></a></li>
    {/maccms:vod}
</ul>
<h2>与<strong>“{$obj.art_name}”</strong>关联的文章</h2>
<ul class="img-list dis">
    {maccms:art num="6" rel="'.$obj['art_rel_art'].'" order="desc" by="time"}
        <li><a href="{:mac_url_art_detail($vo)}" title="{$vo.art_name}"><img src="{:mac_url_img($vo.art_pic)}" alt="{$vo.art_name}"/><h2>{$vo.art_name}</h2><p></p><i>{$vo.vod_from}</i><em></em></a></li>
    {/maccms:art}
</ul>

=======文章分页内容特有标签=======

{$obj['art_page_list'][$param['page']]} 分页内容数组，包含标题备注，分页内容
{$obj['art_page_list'][$param['page']]['title']} 分页标题
{$obj['art_page_list'][$param['page']]['note']} 分页备注
{$obj['art_page_list'][$param['page']]['content']} 分页内容

=======分页内容标签=======
分页代码可用在分类页、筛选页、搜索页、文章内容页、留言本、评论、专题首页等页面，使用前提是页面有包含paging='yes'获取分页数据的标签。
其中包含隐藏参数pageurl=""，视频默认是vod/type，文章分页默认是art/type，分页时必须加入此参数以免分页出错！！！
例如：{maccms:vod num="10" paging="yes" pageurl="vod/type" half="3"} {/maccms:vod}
视频分类页是pageurl="vod/type"
视频筛选页是pageurl="vod/show"
视频搜索页是pageurl="vod/search"
首页是pageurl="index/index"
文章分类页是pageurl="art/type"
文章筛选页是pageurl="art/show"
文章搜索页是pageurl="art/search"
其中half参数是设置显示分页数字页码的个数，不设置默认为5。

<div class="mac_pages">
    <div class="page_tip">共{$__PAGING__.record_total}条数据,当前{$__PAGING__.page_current}/{$__PAGING__.page_total}页</div>
    <div class="page_info">
        <a class="page_link" href="{$__PAGING__.page_url|mac_url_page=1}" title="首页">首页</a>
        <a class="page_link" href="{$__PAGING__.page_url|mac_url_page=$__PAGING__.page_prev}" title="上一页">上一页</a>
        {maccms:foreach name="$__PAGING__.page_num" id="num"}
        {if condition="$__PAGING__['page_current'] eq $num"}
        <a class="page_link page_current" href="javascript:;" title="第{$num}页">{$num}</a>
        {else}
        <a class="page_link" href="{$__PAGING__.page_url|mac_url_page=$num}" title="第{$num}页" >{$num}</a>
        {/if}
        {/maccms:foreach}
        <a class="page_link" href="{$__PAGING__.page_url|mac_url_page=$__PAGING__.page_next}" title="下一页">下一页</a>
        <a class="page_link" href="{$__PAGING__.page_url|mac_url_page=$__PAGING__.page_total}" title="尾页">尾页</a>

        <input class="page_input" type="text" placeholder="页码"  id="page" autocomplete="off" style="width:40px">
        <button class="page_btn mac_page_go" type="button" data-url="{$__PAGING__.page_url}" data-total="{$__PAGING__.page_total}" data-sp="{$__PAGING__.page_sp}" >GO</button>
    </div>
</div>

=======非静态模式下，可获取到的当前登录用户的信息；用户中心里各个界面也可用以下参数{$obj.开头}=======
{$user.user_id} 用户编号
{$user.user_name} 登录名
{$user.user_nick_name} 昵称
{$user.user_email} 邮箱
{$user.user_qq}  QQ
{$user.user_phone} 联系电话
{$user.user_portrait}  头像
{$user.user_points} 积分
{$user.user_reg_time} 注册时间
{$user.user_reg_ip} 注册ip
{$user.user_login_time} 登录时间
{$user.user_login_ip} 登录ip
{$user.user_last_login_time} 上次登录时间
{$user.user_last_login_ip} 上次登录ip
{$user.user_login_num} 登录次数
{$user.user_end_time} vip截止期限
{$user.group_id}用户组编号


=======友情链接列表标签=======
order排列顺序desc倒序，asc正序
by排序依据 id,sort
start从第几条开始
num获取条数
type指定获取类型数据 all所有；font文字链接，pic图片链接；
cachetime自定义缓存时间单位秒

{maccms:link num="10" type="all" order="asc" by="sort"}
   {$vo.link_id}编号
   {$vo.link_name}名称
   {$vo.link_type}类型0文字1图片
   {$vo.link_url}链接
   {$vo.link_sort}排序
   {$vo.link_logo}图标
   {$vo.link_add_time} 添加时间
   {$vo.link_time} 更新时间
{/maccms:link}

=======留言本列表标签=======
order排列顺序desc倒序，asc正序
by排序依据 id,time,reply_time
start从第几条开始
num获取条数
rid关联数据id

{maccms:gbook num="10" paging="yes" order="asc" by="sort"}
   {$vo.gbook_id}编号
   {$vo.gbook_name}昵称
   {$vo.gbook_status}状态0未审核1已审核
   {$vo.gbook_ip}ip地址
   {$vo.gbook_time} 时间
   {$vo.gbook_content} 留言内容
   {$vo.gbook_reply_time} 回复时间
   {$vo.gbook_reply} 回复内容
{/maccms:gbook}


调用方式：
<script>
        $(function(){
            MAC.Gbook.Login = {$gbook.login};
            MAC.Gbook.Verify = {$gbook.verify};
            MAC.Gbook.Init();
        });
</script>


=======评论列表标签=======
order排列顺序desc倒序，asc正序
by排序依据  id, time,up,down
start从第几条开始
num获取条数
rid关联数据id

{maccms:comment num="10" paging="yes" order="asc" by="sort"}
   {$vo.comment_id}编号
   {$vo.comment_mid}模块id，1视频2文字3专题
   {$vo.comment_name}昵称
   {$vo.comment_status}状态0未审核1已审核
   {$vo.comment_ip}ip地址
   {$vo.comment_time} 时间
   {$vo.comment_content} 留言内容
   {$vo.comment_up} 顶数
   {$vo.comment_down} 踩数
   {$vo.comment_report} 举报
{/maccms:comment}

调用方式，例如视频内容页中：

<div class="mac_comment" data-id="{$obj.vod_id}" data-mid="{$maccms.mid}" ></div>
    <script>
        $(function(){
            MAC.Comment.Login = {$comment.login};
            MAC.Comment.Verify = {$comment.verify};
            MAC.Comment.Init();
            MAC.Comment.Show(1);
        });
    </script>


=======明星列表标签=======
order排列顺序desc倒序，asc正序
by排序依据  id, time,time_add,score,hits,hits_day,hits_week,hits_month,up,down,level,rnd,in
start从第几条开始
num获取条数
ids指定id 多个逗号连接
not不抱含id 多个逗号链接
area指定地区
sex指定性别 男 女
letter指定首字母
level指定推荐值 支持多个  1,2
area指定地区 支持多个  大陆,香港
name指定明星支持多个  刘德华,周华健
blood指定血型支持多个  A型,B型
starsign指定星座支持多个  处女座,天蝎座,白羊座
timeadd添加时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
timehits点击时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
time更新时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
hitsmonth月点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsweek周点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsday日点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hits总点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
paging是否分页yes
pageurl分页地址
cachetime自定义缓存时间单位秒

{maccms:actor num="10" paging="no" area="大陆" order="asc" by="sort"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:actor}
=======明星内容页独有标签=======
{$obj.actor_id} 明星id
{$obj.actor_name} 姓名
{$obj.actor_en} 拼音
{$obj.actor_alias} 别名
{$obj.actor_status} 状态
{$obj.actor_lock} 锁定
{$obj.actor_letter} 首字母
{$obj.actor_sex} 性别
{$obj.actor_color} 高亮颜色
{$obj.actor_pic} 图片
{$obj.actor_blurb} 简介
{$obj.actor_remarks} 备注
{$obj.actor_area} 地区
{$obj.actor_height} 身高
{$obj.actor_weight} 体重
{$obj.actor_birthday} 生日
{$obj.actor_birtharea} 出生地
{$obj.actor_blood} 血型
{$obj.actor_starsign} 星座
{$obj.actor_school} 毕业院校
{$obj.actor_works} 主要作品多个逗号相连
{$obj.actor_level} 推荐值
{$obj.actor_up} 顶数
{$obj.actor_down} 踩数
{$obj.actor_score} 平均分
{$obj.actor_score_all} 总评分
{$obj.actor_score_num} 评分次数
{$obj.actor_time} 更新时间
{$obj.actor_time_add} 添加时间
{$obj.actor_time_hits} 点击时间
{$obj.actor_time_make} 生成时间
{$obj.actor_tpl} 自定义模板
{$obj.actor_jumpurl} 跳转url
{$obj.actor_content} 详情
{$obj|mac_url_actor_detail} 获取明星详情页链接




=======角色列表标签=======
order排列顺序desc倒序，asc正序
by排序依据  id, time,time_add,score,hits,hits_day,hits_week,hits_month,up,down,level,rnd
start从第几条开始
num获取条数
ids指定id 多个逗号连接
not不抱含id 多个逗号链接
rid指定关联视频id
actor指定演员名 支持多个 例如  刘德华,成龙
name指定角色名 支持多个 例如 花千骨,黑山老妖
letter指定首字母
level指定推荐值 支持多个  1,2
area指定地区 支持多个  大陆,香港
timeadd添加时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
timehits点击时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
time更新时间 一天前 -1 day，一周前-1 week，一月前-1 month，一小时前-1 hour
hitsmonth月点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsweek周点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hitsday日点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
hits总点击量 大于一千 gt 1000, 小于一千 lt 1000，区间一千二千之间 between 1000,2000
paging是否分页yes
pageurl分页地址
cachetime自定义缓存时间单位秒

{maccms:role num="10" paging="no" rid="'.$obj['vod_id'].'" order="asc" by="sort"}
   内部同下方，{$obj.改为{$vo.开头即可
{/maccms:role}
=======角色内容页独有标签=======
{$obj.role_id} 角色id
{$obj.role_rid} 关联视频id
{$obj.role_name} 角色名
{$obj.role_en} 拼音
{$obj.role_status} 状态
{$obj.role_lock} 锁定
{$obj.role_letter} 首字母
{$obj.role_color} 高亮颜色
{$obj.role_actor} 演员名称
{$obj.role_remarks} 备注
{$obj.role_remarks} 图片
{$obj.role_sort} 排序
{$obj.role_level} 推荐值
{$obj.role_up} 顶数
{$obj.role_down} 踩数
{$obj.role_score} 平均分
{$obj.role_score_all} 总评分
{$obj.role_score_num} 评分次数
{$obj.role_time} 更新时间
{$obj.role_time_add} 添加时间
{$obj.role_time_hits} 点击时间
{$obj.role_time_make} 生成时间
{$obj.role_tpl} 自定义模板
{$obj.role_jumpurl} 跳转url
{$obj.role_content} 详情
{$obj|mac_url_role_detail} 获取角色详情页链接



=======常用处理函数=======
允许使用多个函数，都使用|分隔开
所有图片地址，不管是远程的本地的都建议使用 mac_url_img 来处理。


{:mac_data_count(0,'all','vod')} 获取视频总数量
{:mac_data_count(0,'today','vod')} 获取今日更新视频总数量

{:mac_data_count(0,'all','art')} 获取文章总数量
{:mac_data_count(0,'today','art')} 获取今日更新文章总数量

{:mac_data_count(1,'all')} 获取某个分类下的数据总量，支持视频和文章,传入分类ID
{:mac_data_count(1,'today')} 获取某个分类下的今日更新数据总量，支持视频和文章,传入分类ID

{:mac_url('map/index')} 获取站内链接,参数代表 模块/页面

{$obj.vod_content|mac_url_content_img} 如果使用了第三方附件存储，附件和图片默认url是mac:开头的，此方法将替换为http

{$vo.vod_pic|mac_url_img}  自动转换图片地址

{$vo.vod_content|mac_substring=100}返回截取字符串100个字

{$vo.vod_content|mac_filter_html}返回没有html代码的内容

{$vo.actor|mac_url_create='actor','vod','search','&nbsp;'}
把,号相连的一串字符生成N个搜索链接,后2个参数可以不填写默认是生成vod模块搜索链接。 例子是创建演员搜索链接。支持演员、导演、tag、扩展分类等字段。最后一个参数是生成链接的分隔符。

{$vo.vod_time|mac_day} 自动返回日期

{$vo.vod_time|mac_friend_date} 友好时间提醒 几秒前，几分前，几小时前，几天前。。。

{$vo.vod_year|mac_default='未知'}如果字符串为空，则返回默认字符串

{$user.user_login_ip|mac_long2ip}返回格式化ip地址

{$user.user_id|mac_get_user_portrait}获取用户头像地址


=======常用JS处理函数=======一般用元素的class自动绑定处理事件========

会员-收藏视频内容
<a href="javascript:;" class="mac_ulog" data-type="2" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}">我要收藏</a>
会员-收藏文章内容页
<a href="javascript:;" class="mac_ulog" data-type="2" data-mid="{$maccms.mid}" data-id="{$obj.art_id}">我要收藏</a>
会员-收藏专题内容页
<a href="javascript:;" class="mac_ulog" data-type="2" data-mid="{$maccms.mid}" data-id="{$obj.topic_id}">我要收藏</a>

以下内容一般放到body结尾之前，不用于显示，只用户记录信息。
会员-文章浏览记录
<span style="display:none" class="mac_ulog_set" alt="设置文章内容页浏览记录" data-type="1" data-mid="{$maccms.mid}" data-id="{$obj.art_id}" data-sid="{$param.sid}" data-nid="{$param.nid}"></span>

会员-专题浏览记录
<span style="display:none" class="mac_ulog_set" alt="设置专题内容页浏览记录" data-type="1" data-mid="{$maccms.mid}" data-id="{$obj.topic_id}" data-sid="{$param.sid}" data-nid="{$param.nid}"></span>

会员-视频浏览记录
<span style="display:none" class="mac_ulog_set" alt="设置内容页浏览记录" data-type="1" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}" data-sid="{$param.sid}" data-nid="{$param.nid}"></span>

会员-视频播放记录
<span style="display:none" class="mac_ulog_set" alt="设置视频播放记录" data-type="4" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}" data-sid="{$param.sid}" data-nid="{$param.nid}"></span>

会员-视频下载记录
<span style="display:none" class="mac_ulog_set" alt="设置视频播放记录" data-type="5" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}" data-sid="{$param.sid}" data-nid="{$param.nid}"></span>

视频、文章、专题 顶和踩  通用
<a class="digg_link" data-id="{$obj.vod_id}{$obj.art_id}{$obj.topic_id}" data-mid="{$maccms.mid}" data-type="up" href="javascript:;">
  顶<em class="digg_num">{$obj.vod_up}{$obj.art_up}{$obj.topic_up}</em>
</a>
<a class="digg_link" data-id="{$vod_id}{$art_id}{$topic_id}" data-mid="{$maccms.mid}" data-type="down" href="javascript:;">
  踩<em class="digg_num">{$obj.vod_down}{$obj.art_down}{$obj.topic_down}</em>
</a>

视频、文章、专题点击量显示  通用
总点击量：<span class="mac_hits hits" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}{$obj.art_id}{$obj.topic_id}"" data-type="hits"></span>
日点击量：<span class="mac_hits hits_day" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}{$obj.art_id}{$obj.topic_id}"" data-type="hits_day"></span>
周点击量：<span class="mac_hits hits_week" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}{$obj.art_id}{$obj.topic_id}"" data-type="hits_week"></span>
月点击量：<span class="mac_hits hits_month" data-mid="{$maccms.mid}" data-id="{$obj.vod_id}{$obj.art_id}{$obj.topic_id}"" data-type="hits_month"></span>

前台浏览历史记录调用
<a href="javascript:;" class="mac_history">历史记录</a>

在视频、文章、专题详情页面写入浏览历史记录
<span style="display:none" class="mac_history_set" alt="设置视频历史记录" data-name="[{$obj.type.type_name}]{$obj.vod_name}" data-pic="{$obj.vod_pic|mac_url_img}"></span>
<span style="display:none" class="mac_history_set" alt="设置文章历史记录" data-name="[{$obj.type.type_name}]{$obj.art_name}" data-pic="{$obj.art_pic|mac_url_img}"></span>
<span style="display:none" class="mac_history_set" alt="设置专题历史记录" data-name="{$obj.topic_name}" data-pic="{$obj.topic_pic|mac_url_img}"></span>

访问页面触发定时任务，建议放到首页底部；  由于入口文件名可变，默认是api.php，如需修改请自定义 data-file="xxx.php"
<span style="display: none;" class="mac_timming" data-file="" ></span>

自动获取短网址连接
<input type="text" name="shorten" class="mac_shorten" />
短网址自定义用法，js来获取
<script>
    MAC.Shorten.Get("http://www.maccms.com/",function(r){
        alert(r.data.url_short);
    });
</script>


获取用户记录日志，比如1浏览、2收藏、3想看、4点播、5下载
MAC.Ulog.Get有4个参数type类型0代表全部,page页码,limit每页条数,call回调函数
<script>
    MAC.Ulog.Get(0,1,999,function(r){
        if(r.code == 1){
            $.each(r['list'],function(index,row){
                console.log(row['data']['id'] + '--' + row['data']['name'] + '--' + row['data']['pic'] + '--' + row['data']['link'] + '--' + row['data']['type']['type_name'] + '--' + row['data']['type']['link'] + '--'  );
            });
        }else{
			console.log('获取失败');
        }
	});
</script>


=======预留ajax数据接口，方便瀑布流加载=======
参数
mid:模块1视频2文章3专题
limit:每页条数，支持10,20,30
page:页码，最多不超过20页，防止非法采集
tid:分类id
接口地址是index.php/ajax/data.html?mid=1&page=1&limit=10


=======常用标签技巧========

1，在循环中获取每个分类的数据量
{maccms:type ids="1,2,3,4" order="asc" by="sort" id="vo1" key="key1"}
分成：{$vo1.type_name}；总数量： {$vo1.type_id|mac_data_count=all}；今日数量：{$vo1.type_id|mac_data_count=today}。
{/maccms:type}

2，嵌套循环外层分类内部视频或文章,重点在于外部和内部标签各自设置 id 和 key，系统默认都是vo不适合会导致数据冲掉。
{maccms:type ids="1,2,3,4" order="asc" by="sort" id="vo1" key="key1"}
    {maccms:vod num="10" type="'.$vo1['type_id'].'" order="desc" by="time" id="vo2" key="key2"}
        {$vo1.type_name}:{$vo2.vod_name}；
    {/maccms:vod}
{/maccms:type}

3，嵌套循环一级和二级分类数据

{maccms:type ids="1,2,3,4,5" order="asc" by="sort" id="vo" key="key"} 				  
	{maccms:type parent="'.$vo['type_id'].'" order="asc" by="sort" id="vo2" key="key2"} 
		<li><a href=":mac_url_type($vo2)}">{$vo2.type_name}</a></li>
	{/maccms:type}
{/maccms:type}


4，全站调用全局预留参数，如全局视频扩展分类、地区、语言等数据
{maccms:foreach name=":explode(',',$maccms.vod_extend_class)"}
     {$vo|mac_url_create='class','vod','search'}<br>
{/maccms:foreach}
