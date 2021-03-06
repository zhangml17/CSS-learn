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
### less中使用calc进行变量运算
```
写法：@{变量}
width: calc(~"100% - (@{mainGap} * 3)px");
```
## 弹性布局
### 垂直水平居中
```
.flex {
  display: flex;
  align-items: center; // 垂直居中
  justify-content: center; // 水平居中
}
```
## [vue中以变量引入src地址](https://zhuanlan.zhihu.com/p/88897041)
```
export default {
  data() {
    return  {
      imgSrc: require("../../common/images/logo.png")
    }
  }
}
```
## [非input元素实现placeholder效果](https://blog.csdn.net/m0_37922914/article/details/100152825)
```
ul {
  padding: 5px 0;
  li {
    min-height: 19px;
    font-size: 14px;
    word-break: break-all;
    
    &:empty::before {
      content:"请输入内容...";
      backgrround-color: #efefef;
      color: #000;
      font-size: 12px;
    }
    
    &:focus::before {
      content: none;
    }
  }
}
```
## inline-block问题[参考链接](https://www.cnblogs.com/fantianlong/p/11386994.html)
当使用inline-block布局的元素时，会发现元素之间总是有一定的小间距
### 原因
元素被当成行内元素排版的时候，元素之间的空白符（空格、回车换行等）都会被浏览器处理，根据white-space的处理方式(默认是normal,空白会被浏览器忽略)，HTML代码中的回车换行被转成一个空白符，在字体不为0的情况下，空白符占据一定宽度，所以inline-block的元素之间就出现了空隙。
