### Css实现箭头和气泡

![1615045620552](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615045620552.png)

效果图![1615045662021](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615045662021.png)

![1615045804575](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615045804575.png)

![1615045849932](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615045849932.png)

![1615046164884](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615046164884.png)

![1615046084396](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615046084396.png)

首先我们定义好外部的盒子wrapper

```css
HTML代码：

<div class="wrapper"></div>

CSS代码:

.wrapper {
  width: 200px;
  height: 100px;
  position: relative;
  margin: 100px;
  border: 5px solid #4999ce;
  background-color: #c1d9e9;
  border-radius: 15px;
}

​```![1615046023530](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615046023530.png)
```

然后我们需要为这个盒子添加上之前实现的三角形 bottom那个三角形与盒子颜色相同，其余的三角形选择“隐形”即可。这里可以使用伪元素**::before** 和 **::after**来实现这个效果。这两个元素被默认为行内元素，所以需要更改它们的属性为块级元素,绝对定位。再添加一个小点的白色三角形遮盖上面的三角形，使其露出尖角边框。

![1615046262334](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615046262334.png)

然后再次添加after选择器，用它来形成一个白色的三角形，并按照之前的写法把它定位到上边框上去。 这里需要特别提醒一点，那就是这个白色的小三角形，要比之前的三角形更小一点，至于大小可以自己调整，出来的效果可以了就基本完成了。

```css
.wrapper:after {
  content: '';
  width: 0;
  height: 0;
  border: 20px solid transparent;
  border-bottom-color: #c1d9e9;
  position: absolute;
  top: 0;
  right: 20%;
  margin-top: -36px;
 }
```

![1615046191316](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1615046191316.png)