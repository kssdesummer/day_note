## 选择器

### 基本

- [#id](http://jquery.cuishifeng.cn/id.html)

  id 选择器 , 用#识别	$("div")

- [element](http://jquery.cuishifeng.cn/element.html)

  标签属性	$("div,span,p.jing")

- [.class](http://jquery.cuishifeng.cn/class.html)

  类选择器 用`.`识别	$(".c")

- [*](http://jquery.cuishifeng.cn/all.html)

  识别所有的标签	$("*")

- [selector1,selector2,selectorN](http://jquery.cuishifeng.cn/multiple.html) 

  ```jQuery
  $("div,span,p.jing")
  ```
  

  选择这几个标签下的所有

### 层级

  //空格匹配所有子元素   > 所有子元素     + 紧接着的第一个子元素     ～ 匹配同级别的所有

- [ancestor descendant](http://jquery.cuishifeng.cn/descendant.html)


- [parent > child](http://jquery.cuishifeng.cn/child.html)

- [prev + next](http://jquery.cuishifeng.cn/next_1.html)

- [prev ~ siblings](http://jquery.cuishifeng.cn/siblings_1.html)

### 基本筛选器

- [:first](http://jquery.cuishifeng.cn/first_1.html)	第一个

- [:not(selector)](http://jquery.cuishifeng.cn/not_1.html) 未被选择的

- [:even](http://jquery.cuishifeng.cn/even.html) 偶数索引

- [:odd](http://jquery.cuishifeng.cn/odd.html) 奇数索引

- [:eq(index)](http://jquery.cuishifeng.cn/eq_1.html) 索引值为某数的

- [:gt(index)](http://jquery.cuishifeng.cn/gt.html) 大于给定索引的

- [:lang](http://jquery.cuishifeng.cn/lang.html)1.9+    选择指定语言的所有元素,例如选择器$("div:lang(en)")将匹配<div lang="en"> and <div lang="en-us">（和他们的后代<div>），但不包括<div lang="fr">

- [:last](http://jquery.cuishifeng.cn/last_1.html) 最后一个

- [:lt(index)](http://jquery.cuishifeng.cn/lt.html) 小于给定索引值

- [:header](http://jquery.cuishifeng.cn/header.html) 匹配标题

- [:animated](http://jquery.cuishifeng.cn/animated.html) 匹配所有正在执行动画效果的元素

- [:focus](http://jquery.cuishifeng.cn/focus_1.html) 

  匹配当前获取焦点的元素

  如同其他伪类选择器（那些以":"开始），建议:focus前面用标记名称或其他选择;否则，通用选择("**")是不言而喻的。换句话说，$(':focus')等同为$('*:focus')。如果你正在寻找当前的焦点元素，$( document.activeElement )将检索，而不必搜索整个DOM树。

- [:root](http://jquery.cuishifeng.cn/root.html)1.9+

  选择该文档的根元素。

  在HTML中，文档的根元素，和$(":root")选择的元素一样， 永远是<html>元素。

- [:target](http://jquery.cuishifeng.cn/target.html)1.9+

  选择由文档URI的格式化识别码表示的目标元素。不常用

  如果文档的URI包含一个格式化的标识符，或hash（哈希）， 然后:target选择器将匹配ID和标识符相匹配的元素。  例如，给定的URI http://example.com/#foo， $( "p:target" )，将选择<p id="foo">元素。

### 内容

- [:contains(text)](http://jquery.cuishifeng.cn/contains.html)

  匹配包含给定文本的元素,参数text是用以查找的字符串

- [:empty](http://jquery.cuishifeng.cn/empty_1.html)

  匹配所有不包含子元素或者文本的空元素

- [:has(selector)](http://jquery.cuishifeng.cn/has_1.html)

  匹配含有选择器所匹配的元素的元素

- [:parent](http://jquery.cuishifeng.cn/parent_1.html)

  匹配含有子元素或者文本的元素

### 可见性

- [:hidden](http://jquery.cuishifeng.cn/hidden_1.html)

  匹配所有不可见元素,或者type为hidden的元素,display:none

- [:visible](http://jquery.cuishifeng.cn/visible.html)

  匹配所有可见的元素

### 属性

- [[attribute\]](http://jquery.cuishifeng.cn/attributeHas.html)

  匹配包含给定属性的元素。注意，在jQuery 1.3中，前导的@符号已经被废除！如果想要兼容最新版本，只需要简单去掉@符号即可。

- [[attribute=value\]](http://jquery.cuishifeng.cn/attributeEquals.html)

  匹配给定的属性是某个特定值的元素

- [[attribute!=value\]](http://jquery.cuishifeng.cn/attributeNotEqual.html)

  匹配给定的属性不是某个特定值的元素,等价与not([attr=value])

- [[attribute^=value\]](http://jquery.cuishifeng.cn/attributeStartsWith.html)

  开头

- [[attribute$=value\]](http://jquery.cuishifeng.cn/attributeEndsWith.html)

  结尾

- [[attribute*=value\]](http://jquery.cuishifeng.cn/attributeContains.html)

  包含某些值

- [[attrSel1\][attrSel2][attrSelN]](http://jquery.cuishifeng.cn/attributeMultiple.html)

  同时满足多个条件时同时使用

### 子元素

- [:first-child](http://jquery.cuishifeng.cn/firstChild.html)

  第一个子元素,即若父元素相同则是多个父元素下的第一个子元素,等同于nth-chile(1)

- [:first-of-type](http://jquery.cuishifeng.cn/firstOfType.html)1.9+

  ```
  $("span:first-of-type");
  ```

  即匹配到每一个部分的第一个出现的span

- [:last-child](http://jquery.cuishifeng.cn/lastChild.html)

  最后一个子元素,可多个

- [:last-of-type](http://jquery.cuishifeng.cn/lastOfType.html)1.9+

  即匹配到每一个部分的最后一个

- [:nth-child](http://jquery.cuishifeng.cn/nthChild.html)

  $("ul li:nth-child(3)")匹配从1开始的其父元素下的第三个元素

- [:nth-last-child()](http://jquery.cuishifeng.cn/nthLastChild.html)1.9+

  倒着数

- [:nth-last-of-type()](http://jquery.cuishifeng.cn/nthLastOfType.html)1.9+

  每个部分的倒着数,从1开始

- [:nth-of-type()](http://jquery.cuishifeng.cn/nthOfType.html)1.9+

  同意父元素下的,标签名相同的子元素中的第n个

- [:only-child](http://jquery.cuishifeng.cn/onlyChild.html)

  匹配父元素中唯一的子元素

- [:only-of-type](http://jquery.cuishifeng.cn/onlyOfType.html)1.9+

  同一父元素下的唯一子元素

### 表单

- [:input](http://jquery.cuishifeng.cn/input.html)

  匹配所有 input, textarea, select 和 button 元素

- [:text](http://jquery.cuishifeng.cn/text_1.html)

  单行文本框

- [:password](http://jquery.cuishifeng.cn/password.html)

  类型是type="password"	密码框

- [:radio](http://jquery.cuishifeng.cn/radio.html)

  类型是type="radio"	单选框

- [:checkbox](http://jquery.cuishifeng.cn/checkbox.html)

  类型是type="checkbox"	复选框

- [:submit](http://jquery.cuishifeng.cn/submit_1.html)

  类型是type="submit"	提交按钮

- [:image](http://jquery.cuishifeng.cn/image.html)

  类型是type="image"	图像域

- [:reset](http://jquery.cuishifeng.cn/reset.html)

  类型是type="reset"	重置按钮

- [:button](http://jquery.cuishifeng.cn/button.html)

  类型是type="button"	按钮

- [:file](http://jquery.cuishifeng.cn/file_1.html)

  类型是type="file"	文件域

### 表单对象属性

- [:enabled](http://jquery.cuishifeng.cn/enabled_1.html)

  $("input:enabled")	匹配所有可用元素

- [:disabled](http://jquery.cuishifeng.cn/disabled_1.html)

- [:checked](http://jquery.cuishifeng.cn/checked_1.html)

  匹配所有选中的被选中元素(复选框、单选框等，select中的option)，对于select元素来说，获取选中推荐使用 [:selected](http://jquery.cuishifeng.cn/selected_1.html)

- [:selected](http://jquery.cuishifeng.cn/selected_1.html)

  $("select option:selected") 匹配所有选中的option元素