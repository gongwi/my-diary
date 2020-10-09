# my diary

##目录
##### 小程序运行：	2
1.1登录	2
二、小程序主界面导览：	5
2.1卡片日记显示区	6
2.2页面跳转区	6
2.3日记筛选区	7
三、网站分界面介绍	8
3.1日记编辑页	8
3.1.1 	日期/时间部分	9
3.1.2 	添加图片部分	9
3.1.3 	状态信息栏介绍	12
3.2统计页	14
3.2.1 个人信息板块	14
3.2.2 时间选择器	15
3.2.3日记篇数统计	15
3.2.4写日记的时间点分布统计	16
3.2.5心情晴雨表	16
3.2.6图库	17
3.2.7写日记的地点分布统计	17

一、小程序运行：
1.1登录
 请打开nodejs-portable（请使用2.9.0以上版本的nodejs-portable）中的nodejs-portable.exe，由于小程序功能需求，运行小程序前需安装echarts,mpvue-echarts，在页面内输入npm i echarts mpvue-echarts
 
cd改变文件路径到OneDiary文件夹下，输入npm run build:mp-weixin，当nodejs-portable.exe出现如下界面时:
 
打开微信开发者工具，登录后，点击导航栏的“小程序”，点击调试小程序： 
 
选择“导入项目”，在目录一栏找到OneDiary文件夹下的dist文件夹， 选择build文件夹下的mp-weixin文件夹，点击“导入”：
  
二、小程序主界面导览：
小程序主界面主要分为3个部分，分别是卡片日记显示区、页面跳转区和日记筛选区。
 
2.1卡片日记显示区
即页面中的卡片部分。每一张卡片即为一篇日记，卡片分为两栏，左边由上至下显日、月、年和心情图标，右边则显示日记内容和图片节选。点击右边的两个角可滑动到页面的顶部或底部。

2.2页面跳转区
1.	点击卡片可跳转到该篇日记的详情页。
2.	点击右下角的铅笔图标可进入添加日记页面
3.	页面最下方有两个Tabbar，点击头像可进入个人信息和统计页面。

2.3日记筛选区
1.	点击页面上方的日期和三角形选择选择日期，卡片日记显示区会自动显示所选的月份的所有日记。
2.	下拉页面可进行刷新，卡片日记显示区重新显示所有日记。      

三、网站分界面介绍
3.1日记编辑页
本界面是用户进行填写当天日记或者补写过往日记的界面，主要功能有：记录日记文字、上传该篇日记图片、选择心情、获取用户定位以及获取天气。

3.1.1 	日期/时间部分
在界面顶部，会自动显示用户书写日记当天的日记以及当下的时间。当用户点击日期时，可以选择日期，进行对过去日记补写
  
3.1.1点击页面顶部的日期进行日期选择

3.1.2 	添加图片
（1）用户点击按钮可给自己的日记添加照片，可选择“拍照”或者“从手机相册选择”，添加照片可选择原图或者将图片进行压缩
（2）用户最多能上传九张照片；如：当已经选择5张图片，再次选择图片时，最多只能选择4张
（3）用户点击图片可以进行图片预览
（4）长按图片可对图片进行删除操作
 
3.1.3 	状态信息栏介绍
在页面下方，会有信息栏，显示用户的心情、所处位置、以及此地的天气
 
（1）	心情部分
用户可通过点击，自行选择当天的心情，同时，前方的小图标也会相应发生变化
 
（2）	天气部分
程序会自动获取用户所在位置的天气情况以及温度，显示于页面
 
（3）	定位部分
程序会自动获取用户所在位置，将其所在城市信息显示于页面
 
3.2统计页
本页面由个人信息模块、选择日期功能模块、四个统计板块及图库构成，显示页面如下：
 
3.2.1 个人信息板块
本页面第一个模块为个人信息模块，本模块显示用户头像及昵称

3.2.2 时间选择器
本页面第二个模块为选择日期功能模块，点击个人信息页面，即可看见选择特定时间范围的模块，该模块由时间选择器组成。在时间选择器中选择具体时间范围后，页面中“写日记的时间点分布”和“写日记的地点分布”的统计模块将会出现，并渲染用户数据。
 
3.2.3日记篇数统计
本页面第三个模块为日记篇数统计模块，本模块显示用户已记录的所有日记篇数。
 
3.2.4写日记的时间点分布统计
本页面第四个模块为写日记时间统计模块，点击个人信息页面，并且选择特定时间范围后，即可看见特定时间范围内写日记的时间点分布的模块，该模块主要由展示用户在所选择时间范围内写日记时间点的分布的柱状图组成。图表展示了用户在该时间段内，写日记的时间点在0时到24时这个范围的分布。例如，用户A可以在图表上看见自己在2020年7月这段时间最常在20点这个时间段写日记。
 
3.2.5心情晴雨表
本页面第五个模块为心情指数统计模块，本模块显示用户一段时间内写日记时的心情指数统计，我们将写日记时可选择的每种表情转化为心情指数，对应关系如下：
表情	 	 	 	 	 
代表心情	兴奋	开心	心平气和	难过	生气
心情指数	5	4	3	2	1

心情晴雨表以已选择的年月为x轴，心情指数为y轴，展示该段时间内用户写日记的心情指数情况，从图表可了解用户该段时间的情绪变化。例如：用户从图里了解到某段时间内心情指数起伏很大，则显示该段时间情绪变化过大，可考虑是否及时调整情绪解决困扰等。
 
3.2.6图库
本页面第六个模块为图库，在本界面图库仅显示3张图片，点进图库可查看用户日记上传的所有图片。
 
3.2.7写日记的地点分布统计
本页面第七个模块为写日记的地点分布统计模块，点击个人信息页面，并且选择特定时间范围后，即可看见特定时间范围内写日记的地点分布的模块，该模块主要由展示用户在所选择时间段写日记地点分布的地图组件组成。图表展示了用户在该时间段内，写日记的具体位置分布，滑动滚轮还可以实现放大或缩小地图显示效果。例如，用户A可以在地图组件上看到自己在2020年7月这段时间分别在广州市白云区、广州市番禺区、广州市天河区的xx地点写了日记。
 

