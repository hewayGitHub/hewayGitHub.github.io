---
layout: post
category : tutorial
tagline: "Supporting tagline"
tags : [tutorial]
---
#第一个文章 当然要用markdown#


###基本概念

markdown和邮件的语法基本类似，通过用符合邮件风格的符号来定义格式，我们可以用自然、易读的方式写web文档。主要元素包括标题、段落、列表、引用、代码块、水平分割线、强调、链接、图片等。它们属于两个基本分类，block elements和span elements。
- block elements包括标题、段落、列表、引用、代码块、水平分割线以及直接嵌入的html代码块，它们之间通常需要用空行分隔。  
- span elements包括强调、链接、图片、内嵌代码等。

参考：[某个官方文档](http://daringfireball.net/projects/markdown/syntax#blockquote)

###具体细节

- `#`可以用来表明标题层次，放在句首即可，最多6个
- 连续的文本就是一个段落，段落之间用空行分隔。如果希望在一个段落内部强制换行，在一句末尾留两个以上的空格即可
- 句首加`-, *, +`表示有序列表，用数字后带点号（`1. `）表示有序列表，数字可以全用1，不需要有大小顺序，推荐全用1. 
  如果要在列表里添加列表，缩进即可。
  ```
  1. item1  
  2. item2  
  3. item3  
  ```
- 引用的方法和邮件类似，用`>`，只要注意`>`前后添加空行。

    > 这就是引用了，

- 代码块通过空行之后，添加缩进表示。另外，可以插入代码片段，用ESC键上的反引号` ``code`` `，反引号的数量只要前后匹配就可以。

  ```python
  if __name__ == '__main__':
      print 'i love python'
  ```
- 水平分割线，用`-, *`一行放三个以上即可。注意前面插入空行。

- - -
- 强调，一个`*`是*one*，两个是**two**
- 链接的语法有两种，如下所示。当一个链接需要被多次，或者为了便于管理和美观，可以用第二种方式。
  ```
  [an example](http://example.com/ "Optional Title Here")

  [an example][id]  
  [id]: http://example.com/  "Optional Title Here"
  ```
- 图片其实就是链接，形式如下。Alt属性是图片无法加载时显示的信息，title是鼠标在图片上时显示的信息。
  ```
  ![Alt text](/path/to/img.jpg "Optional title") 
  或  
  ![Alt text][id]
  [id]: url/to/image  "Optional title attribute"
  ```

最后，上面说的这些符号就像定义的关键词，如果想转义，前面加`\`即可。当然上面大不多关键词都是在段首或句首才有效，所以需要转义的情况很少。
