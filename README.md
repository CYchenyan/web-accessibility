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

  