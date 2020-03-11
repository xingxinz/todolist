# todolist
vue实现四个应用
- 1.计数器
- 2.图片切换
- 3.todolist记事本
- 4.查询天气-网络请求应用
  
涉及vue指令 
- v-html {{ }} 内容绑定
- v-model 表单元素双向绑定
- v-for 列表循环
- v-on 事件绑定
- v-if/v-show 显示切换
- v-bind 属性绑定，设置元素的属性（如 src,class，title）

使用axios进行网络请求
遇见问题：axios回调函数中的this已经改变，无法访问到data中数据  
解决方法：把this保存起来，回调函数中直接使用保存后的this即可  
var that = this;
axios.get()
     .then(function(response){
        that.data = response.data;
     })
    .catch(function(err){})
