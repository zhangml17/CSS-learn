# CSS-learn
## 线性渐变
background: linear-gradient(90deg, red, yellow, blue, ...)
## [清除浮动(less写法)](http://blog.sina.com.cn/s/blog_60b35e830101c1r8.html)
```
.clearfix {
  zoom:1;
  &:after {
    visibility:hidden;
    display:block;
    font-size: 0;
    content: '';
    clear: both;
    height: 0;
  }
}
```
## [CSS权重](https://www.jianshu.com/p/983ff63adaa6)
## margin/padding
### 参数含义
```
margin:20px;(上、下、左、右各20px)
margin:20px 40px;(上、下20px；左、右40px)
margin:20px 40px 60px;(上20px；左、右40px；下60px)
margin:20px 40px 60px 80px;(上20px；右40px；下60px；左80px)
padding同理
```
## CSS中calc()方法无效属性值问题
```
width:calc(50%-20px);
这样书写是无效的因为calc中计算的两个因子同运算符号之间必须存在空格；
正确格式为：
width:calc(50% - 20px);
```
## [CSS3中calc在less编译时被计算的问题](https://blog.csdn.net/playboyanta123/article/details/50408335)
