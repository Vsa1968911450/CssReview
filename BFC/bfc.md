BFC 
BLOCK formatting context 块级格式化上下文
形成独立的渲染区域
内部元素不会影响到外界

形成BFC的条件
浮动元素     float 不是none
绝对定位元素 position是absolute或者fixed
块级元素     overflow为hidden的元素
flex元素
inline-block元素

场景 清除浮动
加一个div class clear both
或者css样式 el：after{ clear：both ， content:'', display:block }


flex清除
display flex


Flex-direction 主轴方向
Justify-content 主轴的对齐方式 
Align-items 交叉轴的对齐方式 
flex-wrap 是否换行
