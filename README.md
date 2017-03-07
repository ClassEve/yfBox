# 提示弹出框
这是一个我 **自己封装并在公司网页上使用的弹出框**，第一次写封装代码，可能有一些bug和代码不够简洁的地方，在以后的日子里，我会继续修改和精简

### 1.最简单的prompt提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/defaultDemo.png)
```
yfBox.prompt({
  txt:"这里是默认提示内容"   
})
```

### 2.有两个按钮有提示有标题有mark的提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/defaultDemo.png)
```
yfBox.prompt({
  title: "温馨提示",                 //选填，默认为温馨提示
  txt: "这里是默认提示内容",          //必填
  mark: "这里是底部小字",            //选填，默认为空
  btns: {ok: "确定"，no: "取消" },   //选填，默认为两个按钮，确认和取消，也可以只写一个确认选项
  ok: function(){ },                //点击确定时触发的函数
  no: function(){ }                 //点击取消时触发的函数，以上两个事件都包含默认事件=》弹出框淡出
})
```

