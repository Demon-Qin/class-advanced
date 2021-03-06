## BFC

 BFC在Web⻚⾯上是⼀个独⽴的容器，容器内外互不影响 

和标准⽂档流⼀样，BFC内的元素垂直⽅向的边距会发⽣重叠 

BFC不会与浮动元素的盒⼦重叠 计算BFC⾼度时即使⼦元素浮动也参与计算 

### 创建

 由于块级元素垂直⽅向的边距会发⽣重叠，第⼀个div和第⼆个div之间的 间距并不是15px加上20px后的35px，⽽是20px（较⼤的margin值）， 为了解决边距重叠的问题，让第两个div之间的间距变成35px，可以在div 外⾯创建⼀个BFC

![1614872823858](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1614872823858.png)

设置BFC后

![1614872870284](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\1614872870284.png)

