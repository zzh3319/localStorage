<h2>storage简介<a href="http://www.shdnfw.com/plugin/localStorage/demo.html" target="_blank">本地存储storage(localStorage)的使用示例</a></h2>
<p>storage是基于html5 localStorage本地存储的一个简易改造封装使其变通用的js组件,localStorage 属性允许你访问一个 localStorage 对象，将所需存储数据存储于本地当中，存储在 localStorage 里面的数据没有过期时间（expiration time）</p>

<hr/>

<h3>1、开始工作：</h3>
<p>
  我们需要在页面中引入：
</p>
```html
<script type="text/javascript" src="....../storage.js"></script>
```

<h3>2、通过js调用：</h3>
<p>
  插件中定义全局变量storage，调用本地存储localStorage存、取、删、清可直接使用storage对象直接调用所需方法，如下：
</p>
```javascript
a) 测试数据：
	var _data = {
		name:"勇哥",
		age:24,
		love:"妹子",
		like:[
			"游泳",
			"打球",
			"吹牛"
		]
	}
b) 调用：
	存储：storage.setStorage('testData',_data);
	获取：storage.getStorage('testData');
	删除：storage.removeStorage('testData');
	清空：storage.clearStorage();
```
<h3>3、方法说明：</h3>
<table>
  <tr>
    <th>方法名</th>
    <th>参数</th>
    <th>说明</th>
  </tr>
  <tr>
    <td>storage.setStorage(k,v)</td>
    <td>
      k:存储的数据key值（存储数据的名字）（必填）<br/>
      v:存储的数据（必填）
    </td>
    <td>存储指定名字的数据</td>
  </tr>
  <tr>
    <td>storage.getStorage(k)</td>
    <td>
      k:存储的数据key值（存储数据的名字）（必填）
    </td>
    <td>获取指定名字的本地存储数据</td>
  </tr>
  <tr>
    <td>storage.removeStorage(k)</td>
    <td>k:存储的数据key值（存储数据的名字）（必填）</td>
    <td>删除指定名字的本地存储</td>
  </tr>
  <tr>
    <td>storage.clearStorage()</td>
    <td>无</td>
    <td>清空本地存储的所有数据</td>
  </tr>
</table>

<h3>4、兼容性：</h3>
<p>（兼容性取决于localStorage）</p>
<div>PC端：</div>
<table>
  <tr>
    <th>浏览器</th>
    <th>Chrome</th>
    <th>Firefox (Gecko)</th>
    <th>Internet Explorer</th>
    <th>Opera</th>
    <th>Safari (WebKit)</th>
  </tr>
  <tr>
    <td>localStorage</td>
    <td>4</td>
    <td>3.5</td>
    <td>8</td>
    <td>10.50</td>
    <td>4</td>
  </tr>
</table>
<div>移动端：</div>
<table>
  <tr>
    <th>平台</th>
    <th>Android</th>
    <th>Firefox Mobile (Gecko)</th>
    <th>IE Phone</th>
    <th>Opera Mobile</th>
    <th>Safari Mobile</th>
  </tr>
  <tr>
    <td>localStorage</td>
    <td>2.1</td>
    <td>？</td>
    <td>8</td>
    <td>11</td>
    <td>iOS 3.2</td>
  </tr>
</table>

<h3>5、参考：</h3>
<a href="https://developer.mozilla.org/zh-CN/docs/Web/API/Storage">localStorage-MDN</a>
