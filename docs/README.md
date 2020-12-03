# 学习记录
- [学习记录](#学习记录)
  - [html、css](#htmlcss)
    - [css选择器优先级](#css选择器优先级)
    - [css放在头部和尾部有什么差别](#css放在头部和尾部有什么差别)
  - [js](#js)
  - [算法](#算法)
  - [框架](#框架)
  - [网页](#网页)
  - [Other](#other)
## html、css

### css选择器优先级
!important > 行内样式 > ID选择器 > 类选择器 > 标签 > 通配符
* 全局选择器（通配符*）
* 标签选择器（body， div， p， ul）
* 类选择器（.class）
* ID选择器（#app）

### css放在头部和尾部有什么差别
**href**和**src**的区别
一般加载CSS用**href**，并放在头部；加载script用**src**放在*body*内的下方
> * **href**
> 是hypertext reference的缩写，表示超文本引用，用来建立当前元素和文档间的链接。常用的有*link*， *a*。
> 当CSS使用**href**引用，浏览器会识别该文档CSS并行下载，不会停止对当前文档的加载。
> * **src**
> 是source的缩写，src指向的内容会嵌入到文档中当前标签的位置。常用的有*img*， *script*， *iframe*。
> 当script使用**src**引用，浏览器解析到该元素时会停止对文档的渲染，直到该资源加载完成。这也是将script放底部而不是头部的原因。
> 
把CSS放头部，Script放底部的原因：
> * CSS放头部
> 在加载html生成DOM tree时，就可以同时对DOM tree进行渲染。
> 这样可以防止闪跳，白屏或者布局混乱。
> 
> * JavaScript放底部
> JavaScript可能会改变DOM tree的结构，所以需要一个稳定的DOM tree。
> JavaScript加载后会立即执行，同时会阻塞后面的资源加载。（JavaScript加载和执行的特点）
> *ps：*若要放在头部可
>> * **defer**
>>
>> \*在DOM渲染的同时加载脚本，但是在文档就绪后再去执行，**而且是按照文件先后顺序依次执行**。
>> ```
>> <script src="./index.js" defer></script>
>> ```
>>
>> * **async**
>>
>> \*允许在下载脚本的同时进行对DOM的渲染。但是它将在下载后尽快执行（即JS引擎空闲了立马执行,操作DOM的脚本就不适用async）
>>
>> \*不能保证脚本按顺序执行（这与defer不同）
>> ```
>> <script src="./index.js" async></script>
>> ```

## js

## 算法

## 框架

## 网页

## Other
