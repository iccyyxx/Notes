1. `<!DOCTYPE>` 声明

   - **不是**一个 HTML 标签；
   - 用来告知 Web 浏览器页面使用了哪种 HTML 版本。
   - 位于文档中的最前面的位置，处于 <html> 标签之前。

2. `Window Location`

   - window.location : 所有字母必须**小写**！

   - **只读**属性，返回一个 [`Location`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location) 对象

   - 例如：https://www.nowcoder.com/test/question/done?tid=60518419&qid=2587598#summary
     ```js
     hash: "#summary"
     host: "www.nowcoder.com"
     hostname: "www.nowcoder.com"
     href: "https://www.nowcoder.com/test/question/done?tid=60518419&qid=2587598#summary"
     origin: "https://www.nowcoder.com"
     pathname: "/test/question/done"
     port: ""
     protocol: "https:"
     search: "?tid=60518419&qid=2587598"
     ```

     | --                                                           | --                                                           |
     | ------------------------------------------------------------ | ------------------------------------------------------------ |
     | [`Location.href`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location/href) | 包含整个 URL 的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |
     | [`Location.protocol`](https://developer.mozilla.org/en-US/docs/Web/API/Location/protocol) | 包含 URL 对应协议的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)，最后有一个":" |
     | [`Location.host`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location/host) | 包含了域名的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)，可能在该串最后带有一个":"并跟上 URL 的端口号。 |
     | [`Location.hostname`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location/hostname) | 包含 URL 域名的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |
     | [`Location.port`](https://developer.mozilla.org/en-US/docs/Web/API/Location/port) | 包含端口号的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |
     | [`Location.pathname`](https://developer.mozilla.org/en-US/docs/Web/API/Location/pathname) | 包含 URL 中路径部分的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)，开头有一个“`/"。` |
     | [`Location.search`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location/search) | 包含 URL 参数的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)，开头有一个`“?”` |
     | [`Location.hash`](https://developer.mozilla.org/zh-CN/docs/Web/API/Location/hash) | 包含块标识符的[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)，开头有一个`“#”` |
     | [`Location.username`](https://developer.mozilla.org/en-US/docs/Web/API/Location/username) | 包含 URL 中域名前的用户名的一个[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |
     | [`Location.password`](https://developer.mozilla.org/en-US/docs/Web/API/Location/password) | 包含 URL 域名前的密码的一个 [`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |
     | [`Location.origin`](https://developer.mozilla.org/en-US/docs/Web/API/Location/origin) | 包含页面来源的域名的标准形式[`DOMString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String) |

3. vue组件间通信方式有哪些？

   ```
   EventBus （$emit / $on）
   provide / inject
   props / $emit
   ref 与 $parent / $children
   ```

 	4. JS中创建节点的方式有哪些？
     - cloneNode
     - createElement

#### html5有哪些新特性？

```
Canvas
Web Storage
Web Workers
```

#### js 中现在比较成熟的模块加载方案?

```
CommonJS
AMD
CMD
```

#### Redux遵循的原则有哪些？

```
单一事实来源
状态是只读的
使用纯函数进行更改
```

#### 数组中会改变原数组方法有哪些？

```
sort
pop
```

#### <script>元素

```
src属性可以设置为跟网页再同一台服务器上，也可以在不同的域
使用async属性的脚本不需要等待其他脚本，同时也不阻塞文档渲染
```

#### Chrome浏览器都有哪些进程？

```
GPU 进程
渲染进程
插件进程
```

#### 假设线上代码的分支是master，本地修复bug的分支为fix，上线时下列哪些git操作是正确的

正确答案: A D  你的答案: B (错误)

```
git checkout master; git merge fix;git push origin master;
git checkout fix; git merge master;git checkout master;git push origin master;
git checkout master; git rebase fix;git push origin master;
git checkout fix; git rebase master;git checkout master;git merge fix;git push origin master;
```