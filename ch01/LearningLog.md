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



