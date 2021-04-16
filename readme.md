# 《HTML常用标签》

## a标签
### 属性
1.href 超级链接

网址：https://google.com http://google.com //google.com（该写法需打开开发者工具在network里勾选preserve log）

路径:/a/b/c或a/b/c index.html或./index.html

伪协议:javascritp:代码;

mailto:邮箱

tel:手机号

2.traget 指定在哪个窗口打开页面

_blank 新建窗口打开页面

_top

_parent

_self 在当前窗口打开新页面

3.download 下载该网页（一般不用）

4.rel=noopener

### 作用
* 跳转外部链接
* 跳转内部锚点
* 跳转到邮箱或电话等

## img标签

### 属性

1.src (source的缩写)用来链接加载图片

2.alt 当图片不能成功加载时会出现文字提示

3.width 设置宽度，可以用像素或百分比表示（当没有高度值时，高度自动适应）

4.height 设置高度，像素或百分比表示

5.max-width/height:100%;配合style.css  可以做响应式页面
```css
*{
    padingg:0;
    margin:0;
    box-sizing:border-box;
}
```

### 作用

* 发出get 请求，展示一张图片（查看代码Network-method中可查看到GET）

### 事件

用于监听图片是否加载成功
* 加载成功调用 onload
* 加载失败调用 onerro

```html
<body>
<img id="xxx" src="QQ图片20190121101923.jpg" alt="太白" height="200px">
    <script>
        xxx.onload = function () {
            console.log("图片加载成功");
        };
        xxx.onerro = function () {
            console.log("图片加载失败");
        };
    </script>
    </body>
```
* 此处要给img 加个id 名称！

## table标签

### 属性

* 是一个表格标签
* thead
* tbody
* tfoot
* tr 写在thead/tbody/tfoot中 (tabke row 一行内容)
* th 展示表头内容
* td (table data 表格数据)

### 相关样式css

table-layout

border-collapse

border-spacing
