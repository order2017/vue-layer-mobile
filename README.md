#vue-layer
vue弹出层插件,包含toast loading dialog等浮层控件

demo地址:http://jianghai.wao021.cn/app/layer.html

#使用方法
```javascript
import from 'vue-layer/need/layer.css'
import vue-layer from 'vue-layer/index'
Vue.use(vue-layer)
```

toast:
文字和图标:
```javascript
this.$layer.toast({
  icon: 'icon-check', // 图标clssName 如果为空 toast位置位于下方,否则居中
  content: '提示文字',
  time: 2000 // 自动消失时间 toast类型默认消失时间为2000毫秒
})
```

loading: 
```javascript
this.$layer.loading('加载中...')
```
dialog:
```javascript
this.$layer.dialog({
  title: ['这是标题', 'background:red;'], // 第一个是标题内容  第二个是标题栏的style(可以为空)
  content: '这是内容',
  btn: ['确定']
  time: 2000
})
// 如果有btn
.then(function (res){
  // res为0时是用户点击了左边  为1时用户点击了右边
  let position = res === 0 ? 'left' : 'right'
  console.log(position)
})
```
参考:开源插件layer-mobile http://layer.layui.com/mobile/

