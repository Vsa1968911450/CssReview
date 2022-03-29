BFC 
BLOCK formatting context 块级格式化上下文
形成独立的渲染区域
内部元素不会影响到外界

形成BFC的条件
浮动元素     float 不是none
绝对定位元素 position是absolute或者fixed
块级元素     dispaly不是visible
flex元素
inline-block元素

场景 清除浮动
加一个div class clear both
或者css样式 el：after{ clear：both ， content:'', display:block }
