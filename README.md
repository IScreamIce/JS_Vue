简单的使用Vue.js教程

在这个HTML中，我们使用Vue做到了以下几点：

1、var data={key:val,key:val}                  申请数据结构,并存放值 
2、new Vue({data:var})                         Vue对象引用var数据结构 
3、在其他作用域范围内，对数据结构以及通过Vue操作(改变)数据结构中的数据 
4、vm.$watch('attribute name',function(){})    监控属性值的改变,触发回调方法 
5、在new Vue({el: '#id name'})                 通过id将元素与Vue实例绑定(内部元素可以访问Vue实例) 
6、{{name}}                                    通过名字，去获得Vue引用的数据结构内的值，获得值 
7、v-if="boolean"                              通过v-if指令，选择元素某些状态是否显示 
8、v-html {{name}}                             默认是内容转文本，如果是html元素需要v-html指令说明
9、v-on:click="name=val"                       指令绑定点击事件，当点击时，通过name修改数据结构中的值 
10、v-bind-href="url"                          给a链接绑定url，url是从data获得，而不是写死的，而data是可以改变的
11、尝试v-bind-href的简写:href一样效果
12、v-on:click="functionname"                  之前是触发点击事件修改值，现在给绑定方法，方法需要在Vue实例内的methods书写，绑定受Vue管理的方法 
13、{{name}}不同于直接去数据结构取值，这个name也称计算属性，是Vue实例中的computed中的方法，意思是，经过计算return返回的值，这不是单纯取值而是取计算后的返回值 
14、v-bind:class="name"                        绑定样式，样式是在data数据中说明的，说明样式是可改变的，而不是写死的 
15、v-on:click                                 当单机时取修改v-bind:class数据结构中的样式数据结构
16、v-for="var in listdata"                    循环数组，数组中每一个变量寄存在var元素身上，var元素即数组内的每个下表元素，元素.key取得值
17、v-for="(var,index) in listdata"            不仅将循环数组的每一个元素，放在var身上，并且还拥有一个下班寄存在index身上，下标按0走

说明：data中的数据一旦修改，其引用处都会修改，无需操作手心修改值的问题

对比： vue与css与html：vue的操作，可以说是从data中拿数据，而data是容易改变的。而html与css是写死的。比如a的链接与css的引用

vue与jquery：vue做的事情，jquery也能做，区别是，jquery是依赖dom对象中。dom找到元素对象进行属性修改。而vue则不是，这有点像元素绑定在vue上，改vue等于触发观察者模式。 一个是依赖dom查找并修改，一个是类似观察者模式的绑定。修改后，响应分发。将会省事许多

vue的取值是通过{{data中的name | 计算值属性name}}

元素绑定Vue的单击事件等方法，此类方法需要在当前元素绑定的Vue实例中书写。受Vue管理才能绑定。比如methods与computed

但Vue给元素绑定，就不需要了，比如Vue.$watch("name",function(){})

取值不仅限于绑定的元素通过{{}}取，在script中是可以直接对vue对象产生操作的。

以上就是HTML中使用vue的总结了
