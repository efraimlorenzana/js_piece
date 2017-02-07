# Document.prototype.createTextNode

## 标准
[WHATWG: createTextNode](https://dom.spec.whatwg.org/#dom-document-createtextnode)

## 定义和用法
文档节点的 createTextNode 方法用于创建文本节点。

- 语法：document.createTextNode(data)
- 参数：文本内容（DOMString）
- 返回值：文本节点

## 属性描述
createTextNode 方法可配置，可枚举，可重写。
```javascript
// Object.getOwnPropertyDescriptor(Document.prototype, 'createTextNode') 的结果如下：
var result = {
  configurable: true,
  enumerable: true,
  writable: true,
  value: Document.prototype.createTextNode
}
```
## 注意事项
1. data 含有的元素标签不会被解析，会直接显示，所以用 createTextNode 可以增加安全性。

## 示例代码
createTextNode 方法用于创建文本节点。
```html
<!--运行前-->
<div class="js-wrap"></div>
<script>
  var newTextNode = document.createTextNode('jszhou');
  document.querySelector('.js-wrap').appendChild(newTextNode);
</script>

<!--运行后-->
<div class="js-wrap">jszhou</div>
<script>
  var newTextNode = document.createTextNode('jszhou');
  document.querySelector('.js-wrap').appendChild(newTextNode);
</script>
```

## 参考资料
1. [MDN: createTextNode](https://developer.mozilla.org/en-US/docs/Web/API/Document/createTextNode)