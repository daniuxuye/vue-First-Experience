# Vue-初体验/两个版本的区别
在我们使用 vue时，我们可以引用两个不同版本的 Vue，分别是 Vue完整版（vue.js）和 Vue（vue.runtime.js ）非完整版，那么它们的区别是什么呢，今天我们就来分析下这两个不同版本之间的区别。  

**Vue的两个版本**
* 运行时版本vue.runtime.js
* 完整版vue.js
  


<h1 class="heading" data-id="heading-5">两个版本的区别</h1>
<table>
<thead>
<tr>
<th style="text-align:center"></th>
<th>Vue完整版</th>
<th>Vue非完整版</th>
<th>评价</th>
</tr>
</thead>
<tr>
<td style="text-align:center">特点</td>
<td>有compiler</td>
<td>无compiler</td>
<td>complier占40%体积</td>
</tr>
<tr>
<td style="text-align:center">视图</td>
<td>写在HTML里 或者写在template选项</td>
<td>写在render函数里用h来创建标签</td>
<td>h是尤雨溪写好传给render的</td>
</tr>
<tr>
<td style="text-align:center">cdn引入</td>
<td>vue.js</td>
<td>vue.runtime.js</td>
<td>文件名不同，生成环境后缀为.min.js</td>
</tr>
<tr>
<td style="text-align:center">webpack引入</td>
<td>需要配置alias</td>
<td>默认使用此版</td>
<td>尤雨溪配置的</td>
</tr>
<tr>
<td style="text-align:center">@vue/cli引入</td>
<td>需要额外配置</td>
<td>默认使用次版本</td>
<td>尤雨溪，蒋豪群配置的</td>
</tr>
</table>

***
## template 和 render 怎么用


>Vue非完整版
```
new Vue({
 render (h) {
 return h('div', this.hi)
 }
})
```
>Vue完整版
```
new Vue({
 template: '<div>{{ hi }}</div>'
})
```

## 下面向大家安利一个网址
>https://codesandbox.io/s/  

这是一款很方便的在线编辑平台。
***
**不要登录，登录都只能创建50给应用，不登录无限用。** 

 进去后点VUE图标，下面就可以自由发挥了。

那如果我想把应用下载到本地怎么做呢?
1. 点击左上角`file`然后点击`Export to ZIP`
2. 你会下载到一个源代码的包，自己解压缩把。
3. 把文件托到自己本地的剪辑器里去，自己爱怎么弄怎么弄去吧。





