## 消息气泡拖拽组件
基于vue实现的仿QQ消息气泡拖拽插件。
#### 安装
```
npm install vue-bubble
```
#### 使用
1. 入口vue引入
```
const vueBubble from 'vue-bubble'
Vue.use(vueBubble)
```
2. 组件中使用
v-bubble指令对应的是一个对象。该对象有如下可选值：
* value
> 必选，消息气泡显示的值。

* show
> 可选，是否显示消息气泡，true为显示，false为隐藏。需要注意的是，该属性优先级大于value
比如，value=0，show为true，这种情况show起作用，value忽略，故气泡显示。

* afterHide
> 可选，回调函数，气泡拖拽消失之后执行的回调，一般用于重置。

```
<i v-bubble="{show:item.show,afterHide: (hide.bind(this,item)),value : item.count}" class="msg"></i>
```
