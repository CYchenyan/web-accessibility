# web-accessibility
无障碍网页（Web Accessibility ，缩写：A11Y）指在物理条件和技术条件限制下，保证网站达到最佳可用性的实践。

[MDN介绍](https://developer.mozilla.org/zh-CN/docs/Learn/Accessibility/What_is_accessibility)

## HTML和可访问性

##### 1. 使用HTML语义化标签
  * 更便于开发 — 使HTML更易于理解，并且可以毫不费力的获得一些功能。
  * 更适配移动端 — 语义化的HTML文件比非语义化的HTML文件更加轻便，并且更易于响应式开发。
  * 更便于SEO优化 — 比起使用非语义化的<div>标签，搜索引擎更加重视在“标题、链接等”里面的关键字，使用语义化可使网页更容易被用户搜索到。
##### 2. 良好的语句
  * 文本内容使用标准的标题、段落、列表的语义结构
  * 页面布局使用标准的header、footer、main、nav、article语义化标签
  * 尽量使用默认情况下浏览器允许用户通过键盘操作的UI控件。主要包括与用户交互的文档部分。通常是按钮、链接和表单控件
  * 使用`tabindex=0` `tabindex=-1`重新建立键盘的可访问性。 通过`document.activeElement.onclick（）`运行存储在按钮的onclick处理函数中的函数。
  * 使用有意义的文字标签
  * 可访问的表格
  * 文本替代品-针对媒体元素，例如图片、视频
  * 使用空的alt属性，使屏幕阅读器读出完整的url地址

## css 和 javascript 无障碍最佳实践
  [MDN介绍](https://developer.mozilla.org/zh-CN/docs/Learn/Accessibility/CSS_and_JavaScript)

## WAI-ARIA

WAI-ARIA 是一项技术，它可以通过浏览器和一些辅助技术来帮助我们进一步地识别以及实现语义化，这样一来能帮助我们解决问题，也让用户可以了解发生了什么

##### 1. WAI-ARIA定义了一组可作用与html元素上的额外的属性，用于帮助提供额外的语义化以及改善缺乏的可访问性。主要包括：

* __角色：__ 定义了元素是什么或者具有什么功能
* __属性：__ 定义了元素的属性，可用于赋予元素额外的含义或语义。
* __状态：__ 定义元素当前条件的特殊属性

___状态和属性的差异：属性通常在整个app的生命周期中不会改变，而状态可以通过jacascript修改。例如：属性：aria-required="true";状态：aria-disabled:"true"___

##### 2. 使用WAI-ARIA的场景

* 作为地标用来标示语义化标签的含义，甚至超越标签的含义。例如：`search`, `tabgroup`, `tab`, `listbox`
* 动态内容更新，使用`aria-live`来通知动态内容的更新
___off: 默认值，更新不会提醒。___
___polite:  只有用户空闲的情况下提醒。___
___assertive: 尽快提醒。___
___rude: 会以打断用户操作的方式直接提醒。___
* 优化键盘的无障碍操作，例如使用`tabindex`使div等默认不可被键盘聚焦的元素获取焦点
* 非语义控件的可访问性，例如当div与css/js有比较复杂的ui操作时，屏幕阅读器很难找到语义的内容，可以通过添加`role`，或者`aria-required`等属性提高网页的可访问性

## Accessible multimedia
