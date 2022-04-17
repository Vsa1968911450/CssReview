移动端手机屏幕宽度不一样 
document.documentElement.clientWidth
然后赋值给屏幕宽度 
样式就写rem


px 固定像素
em 相对于父元素 em的参照物不一样
rem相对于根元素 html元素
vw 视口的宽度 和百分比一样 相对的单位 
vh 视口高度 和百分比一样 相对的单位

vh和 百分比的区别
百分比是相对于父元素 如果父元素 和 视口不一样单位 表现就不一样
vh是相对于视口宽度

屏幕尺寸 屏幕对角线的长度
物理像素 屏幕成像的最低单位
屏幕密度 ppi
css像素 px的相对单位
设备像素比（dpr） 设备像素比  = 物理像素 / 设备独立像素  可以通过 window.devicePixelRatio获取

处理rem适配 postcss-px2rem rem的插件
rem 是和html元素下的font-size有关 
通过dpr实现缩放比 scale = 1 / dpr  物理像素
dpr = 1/ window.devicepixelratio  达到缩放视口
然后动态计算html的fontr-size font-size = 视窗宽度 / 10
rem基准值 = clientwidth / 10 = 设计稿尺寸 / x 
2 clientwidth / 100 当做rem
计算font-size 总是以100 获取宽度 / 100 来获取除了数6.4
document.documentElement.style.fontSize = document.documentElement.clientWidth / 6.4 + 'px';

解决1px的方法 
1 媒体查询 查询 当前dpr的值 通过媒体查询去解决 比如设置border大小
2 或者构建一个伪元素 border为1px tarnsform 50%
3 计算rem 
高清屏图片模糊
1 image=set

2 img的srcset属性

3 使用svg