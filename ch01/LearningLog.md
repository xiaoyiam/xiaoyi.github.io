###  1.父元素和子元素

![](https://ipic101-1253790954.cos.ap-beijing.myqcloud.com/xiaoyi/2020-03-19-Snip20200319_49.png)



CSS中，元素是自上而下的，上一层级的元素是下一层级元素的父元素（parent element），下一级是上一级的子元素(child element)
>“ In CSS, styling rules flow down from parents to children unless another style interrupts and takes priority.”

>摘录来自: Lee Donahoe and Michael Hartl. “Learn Enough CSS & Layout to Be Dangerous。” Apple Books.

###  2.DRY 原则

DRY 原则，即 don't repeat yourself。比如下面这段代码 ：

    <div  style="border: 1px  solid  black;">
    <div  style="border: 1px  solid  black;">
    <div  style="border: 1px  solid  black;">

三个div设置成同样的格式，但是重复了三次。根据DRY原则，把这三个操作通过一次操作来完成。这里就用到

      <style>
         div{
             border:1px  solid  black;
          }
      </style>

把这三个  inline css  放到一个CSS文件中。

###  3.声明
![](https://ipic101-1253790954.cos.ap-beijing.myqcloud.com/xiaoyi/2020-03-19-Snip20200319_50.png)

###  4.怎么给列表里面的字体设置格式

    <ol>
        <li>我想被设置成红色</li>
    </ol>

可以在style里面进行设置，比如像下面这个样子

    <style>
      div ol{
          color:red;
      }
    </style>


###  5.如何选择特定的某个（或某些）元素进行格式的精准设置？

1. 如果要设置具体的某一个元素，可以给这个元素添加一个  id； id=“xx”
2. 如果要设置一类（比如一级标题）的元素格式，那就要考虑使用 class（类）进行设置。  class=“yy”

>“how can we apply styling to specific elements rather than to every single one?
There are two methods, one that targets only one element per page—the id (or “identification”) selector17—and one able to target multiple elements—the class selector. Let’s edit our example HTML to add this kind of targeting to our page.
Ids and classes are always applied only to the opening tag of an element, and they always have the same format. We’ll use the div tag for concreteness:”
“We see here that both ids and classes consist of key/value pairs, where each value is a string that serves as a label for the id or class. In this case, the key id has value "foo" and the key class has value "bar".”



>摘录来自: Lee Donahoe and Michael Hartl. “Learn Enough CSS & Layout to Be Dangerous。” Apple Books.

    <div  id="foo"  class="bar">
      .
      .
      .
    </div>

但是请注意每一个元素只能有一个id  ；言外之意就是每一个元素可以有多个 class

![](https://ipic101-1253790954.cos.ap-beijing.myqcloud.com/xiaoyi/2020-03-20-Snip20200320_51.png)

在css样式中进行样式指定的时候，指定id，需要在前面加上 #
