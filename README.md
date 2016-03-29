## 网易教育产品部

- 正确测量大小宽高距离等数值，正确还原视觉效果
- 页面兼容IE8+，FireFox，Chrome
- 正确使用语义化标签，CSS文件内部规范化分类
- JS未使用任何框架，注释完整
- 课程列表的获取、登录以及关注均通过调用Ajax进行
- 作品展示：http://lizhg.com/demo/edu/
- 作品代码：http://github.com/lizhg/edu


### 关于

---

#### 1 功能点

##### 1.1 关闭顶部通知条

点击顶部通知条的“X 不再提醒后”，刷新页面不再出现此通知条（使用本地cookie实现）。点击项的hover效果见视觉稿

##### 1.2 关注 “网易教育产品部” /登录

- 点击关注按钮：首先判断登录的cookie是否已设置（loginSuc）
- 如果未设置登录cookie，则弹出登录框，使用给定的用户名和密码（需要表单验证）调用服务器Ajax登录，成功后设置登录cookie
- 登录成功后，调用关注API，并设置关注成功的cookie（followSuc）
- 登录后“关注”按钮变成不可点的“已关注”状态。按钮的hover效果见视觉稿


##### 1.3 顶部右侧导航及内容区各产品的“了解更多”

点击导航中的“网易公开课”，“网易云课堂”，“中国大学MOOC”，新窗口打开对应的页面。对应的跳转链接如下，点击项的hover效果见视觉稿。点击“了解更多>”的跳转链接及打开方式相同。

- 网易公开课：http://open.163.com/
- 网易云课堂：http://study.163.com/
- 中国大学MOOC：http://www.icourse163.org/


##### 1.4 轮播图

三张轮播图轮播效果：实现每5秒切换图片，图片循环播放；鼠标悬停某张图片，则暂停切换；切换效果使用入场图片 500ms 淡入的方式。点击后新开窗口打开目的页面，对应的跳转链接如下，

- banner1：http://open.163.com/
- banner2：http://study.163.com/
- banner3：http://www.icourse163.org/


##### 1.5 左侧内容区tab切换

点击“产品设计”或“编程语言”tab，实现下方课程内容的更换。tab项的hover及选中效果见视觉稿，tab项对应的课程卡片数据见本文档的数据接口列表


##### 1.6 查看课程详情

鼠标悬停“产品设计”或“编程语言”tab下的任意课程卡片，出现浮层显示该课程的课程详情；鼠标离开课程详情浮层，则浮层关闭。课程卡片即详情浮层的效果见视觉稿，课程卡片及详情数据见本文档的数据接口列表


##### 1.7 右侧“机构介绍”中的视频介绍

点击“机构介绍”中的整块图片区域，调用浮层播放介绍视频。图片的hover效果见视觉稿，浮层中调用的播放器（不做浏览器兼容，可用html5）及视频内容接口见本文档的数据接口列表

##### 1.8 右侧“热门推荐”

实现每次进入或刷新本页面，“热门推荐”模块中，接口返回20门课程数据，默认展示前10门课程，隔5秒更新一门课程，实现滚动更新热门课程的效果。课程数据接口见本文档的数据接口列表


##### 1.9 页面布局动态适应

根据浏览器窗口宽度，适应两种视觉布局尺寸。窗口宽度<1205时，使用小屏视觉布局； 窗口宽度>=1205时，使用大屏视觉布局。布局示意图见视觉效果

---

#### 2 要求

##### 2.1 效果要求

正确还原视觉效果，正确测量大小宽高距离等数值，文字边框背景等颜色能正确取色

##### 2.2 功能要求

按照效果图和上面的功能点完成所有功能（可以不考虑跨域问题）


##### 2.3 兼容性要求

页面兼容IE8+、FF、Chrome，允许圆角、阴影只在高版本浏览器中实现

##### 2.4 HTML要求

完善头部信息，代码缩进，正确使用语义化标签及实体，考虑SEO需要，正确嵌套标签，正确使用标签属性，规范的注释格式

##### 2.5 CSS要求

CSS文件内部规范化分类，命名和格式规范化，注释清晰，合理优化代码

##### 2.6 JS要求

1. 本作业要求不使用任何的JS框架
2. JS代码要求有统一的命名规范
3. JS代码要求整洁、紧凑、可读性好
4. JS代码要求注释完整

##### 2.7 其他要求

代码简洁性、通用性、扩展性、可读性、可维护性