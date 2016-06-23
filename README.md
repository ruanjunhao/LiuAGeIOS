# 六阿哥网iOS版

## 项目介绍

这个项目基于我写的另一个项目 [BaoKanIOS](https://github.com/6ag/BaoKanIOS) 代码基础上进行开发的。经过测试后的代码会逐步更新到 [BaoKanIOS](https://github.com/6ag/BaoKanIOS) ，所以学习建议参考这个项目。数据来源我的个人网站 [六阿哥网](http://www.6ag.cn)  。

**提示：** 项目正在开发阶段，接口修改可能比较频繁。如果发现项目是因为接口修改报错，请重新 `clone` 项目即可。

### AppStore

<a target='_blank' href='https://itunes.apple.com/app/id1120896924'>
<img src='http://ww2.sinaimg.cn/large/0060lm7Tgw1f1hgrs1ebwj308102q0sp.jpg' width='144' height='49' />
</a>

### 主要技术

+ `tableView` / `scrollView` 手势冲突处理
+ 主流选项卡切换控制器、加载数据方式
+ 分类栏目自定义管理、 `collectionView` 排序
+ 主流图片浏览器处理、各种手势、用户体验增强
+ 使用 `sqlite` 数据库缓存列表页、幻灯片、新闻正文、图库正文数据
+ `js` 与 `swift` 交互，实现正文加载图片占位和缓存处理，并添加图片点击交互
+ 集成 `JPush` 实现各种远程推送，集成 `ShareSDK` 实现社交分享、第三方登录

### 项目结构

+ LiuAGeIOS *项目主目录*
+ ------------ Resource *资源目录*
+ ------------ Classes *项目所有类文件*
+ ---------------------- Application *应用级别类*
+ ---------------------- Vendor *第三方库*
+ ---------------------- Categories *分类*
+ ---------------------- Model *公共模型*
+ ---------------------- Utils *工具类*
+ ---------------------- Module *模块目录*
+ ------------------------------------- Main *主模块*
+ ------------------------------------- News *资讯模块*
+ ------------------------------------- Profile *个人中心模块*

### 开发环境

*XCode7.3* + *swift2.2* ，如果下载项目后，编译失败，请检查 `XCode` 版本是否满足。

### 特别注意

资讯正文部分的图片是用 `YYWebImage` 进行缓存管理的，而由于 `YYWebImage` 的缓存策略原因，低于 `20kb` 的文件不会直接存文件，所以我们必须要修改框架原文件。修改`YYCache` -> `YYDiskCache.m` 的第 `171` 行，将 `1024 * 20` 修改为 `0` 即可。

### 讲解文章

+ [使用NSKeyedArchiver缓存app用户账号数据](https://blog.6ag.cn/1545.html)
+ [使用SQLite缓存数据分析与实现](https://blog.6ag.cn/1551.html)
+ [网易新闻app内容页实现分析与代码实现 完成图片缓存和交互](https://blog.6ag.cn/1514.html)

### 主流控制器切换

![image](https://github.com/6ag/LiuAGeIOS/blob/master/1.gif)

### 自定义栏目管理

![image](https://github.com/6ag/LiuAGeIOS/blob/master/2.gif)

### 性感的侧栏，无手势冲突

![image](https://github.com/6ag/LiuAGeIOS/blob/master/3.gif)

### 支持各种手势的图片浏览器

![image](https://github.com/6ag/LiuAGeIOS/blob/master/4.gif)

### 模仿网易新闻的内容正文

![image](https://github.com/6ag/LiuAGeIOS/blob/master/5.gif)

### 便捷修改字体

![image](https://github.com/6ag/LiuAGeIOS/blob/master/6.gif)

### 上拉退出详情

![image](https://github.com/6ag/LiuAGeIOS/blob/master/7.gif)
