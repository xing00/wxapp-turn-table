# wxapp-turn-table
微信小程序大转盘，使用css3创建，非canvas
小程序的canvas非常坑，故选择使用css3进行大转盘实现。
主要的实现方法就是使用div来画三角形，然后外层使用overflow:hidden。
此大转盘最少支持1个奖品，最多支持8个奖品，超过会发生什么事我就不知道了。
另外转盘的大小是设计师给出的比较合适的大小，若要改变大小，请修改.plate-box这个标签的style属性的
top、transform-origin、border-top、border-left、border-right。

border-left、border-right的440是转盘的长宽，这两个属性只需要修改成你想要的大小，
top、transform-origin、border-top这三个属性在调整的时候，需要将外层的overflow先去掉，然后先调整transform-origin，
一点点地调，让外层的对齐，对齐之后的数字填入top跟border-top即可。
主要修改2、4、6、8这4种情况就可以了，8个以上的情况跟8个是一样的，因为实现得不是很理想，所以修改转盘大小有很多地方要改动。

使用的时候在lottery传入奖品的数组即可，会自动生成转盘。
这个转盘目前实现得不是很好，有空我会找找其他方法，尽量做到修改转盘大小不用修改那么多东西。
