- **基础记录**
    - **[addEventListener](https://developer.mozilla.org/zh-CN/docs/Web/API/EventTarget/addEventListener)监听器的所有[触发事件](https://developer.mozilla.org/zh-CN/docs/Web/Events)、 [querySelector](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/querySelector)**
    - [**hasOwnProperty**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty)只拿自己定义的属性，忽略掉那些从原型链上继承到的属性
    - [**for in 拿下标， for of 拿值**](https://www.jianshu.com/p/ee21c4c86d5d)
        - for in得到对对象的key或数组,字符串的下标
    - **link与@import区别**
        - import可以用在css，而link不能http://www.divcss5.com/rumen/r431.shtml
        - import会增加HTTP请求 https://www.cnblogs.com/xuqw/p/11794612.html（此链接包括媒体查询的属性）

- **文档对象模型 (DOM)**
    - Element元素宽度
        - [Element.clientWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/clientWidth) 包括内边距(padding)、但不包括边框(border)、外边距 margin 和竖直方向滚动条(scrollbar)（如果存在的话）
        - [Element.scrollWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/scrollWidth) 同上之外，它还可以包括伪元素的宽度，例如::before或::after。 如果元素的内容可以适合而不需要水平滚动条，则其scrollWidth等于clientWidth
![image](https://user-images.githubusercontent.com/6947480/89880587-feb60180-dbf6-11ea-8c68-5a1fbbc03467.png)
clientWidth和scrollWidth共用此图

        - [Element.offsetWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLElement/offsetWidth) 包含内边距(padding)、边框(border)、竖直方向滚动条(scrollbar)（如果存在的话）
![image](https://user-images.githubusercontent.com/6947480/89880632-0aa1c380-dbf7-11ea-9242-3686168b164d.png)

        - [Window.innerWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/innerWidth) 窗口的内部宽度，包含垂直滚动条

            ```jsx
            // 返回视口的宽度
            var intFrameWidth = window.innerWidth;

            // 返回一个框架集内的框架的视口宽度
            var intFrameWidth = self.innerWidth;

            // 返回最近的父级框架集的视口宽度
            var intFramesetWidth = parent.innerWidth;

            // 返回最外层框架集的视口宽度
            var intOuterFramesetWidth = top.innerWidth;
            ```

        - `[Window.outerWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/outerWidth)` 整个浏览器窗口的宽度，包括侧边栏（如果存在）、窗口镶边（window chrome）和调正窗口大小的边框（window resizing borders/handles）
        - 如果需要获取除去滚动条和边框的窗口宽度，请使用根元素 <html> 的clientWidth 属性。`document.querySelector('html').clientWidth`
        - [JS,Jquery获取各种屏幕的宽度和高度](https://www.cnblogs.com/fuyuanming/articles/5453756.html)
- **VS Code记录（含快捷键）**
    - 触发建议 默认快捷键是“ctrl+space”，window系统会快捷键冲突，因为可以自定义修改，我现在改为“alt+/”
    - 删除行 "ctrl+shift+k"
- **[Emmet语法](https://www.cnblogs.com/Arunoido/p/10753873.html)**
- [**Flex布局**](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
