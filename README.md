# 一、prompt弹出框
### 1.最简单的prompt提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/defaultDemo.png)
```
yfBox.prompt({
  txt:"这里是默认提示内容"   
})
```

### 2.有两个按钮有提示有标题有mark的提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/markDemo.png)
```
yfBox.prompt({
  title: "温馨提示",                 //选填，默认为温馨提示
  txt: "这里是默认提示内容",          //必填
  mark: "这里是底部小字",             //选填，默认为空
  btns: {ok: "确定"，no: "取消" },    //选填，默认为两个按钮，确认和取消，也可以只写一个确认选项
  ok: function(){ },                 //点击确定时触发的函数
  no: function(){ },                 //点击取消时触发的函数，以上两个事件都包含默认事件=》弹出框淡出
  closeBtn:"none"                    //选填，如果写none，则不会出现右上角关闭按钮，不填默认显示
})
```

### 3.一个按钮的prompt提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/onebtn.png)
```
yfBox.prompt({
  txt:"这里是默认提示内容",
  btn:{ok:"确定"}
})
```

# 二、tip框
注意：除了info没图标，其他都有对应图标；tip框里一定没有按钮，最后一个参数可以设置自动消失的时间
### 1.默认info框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/infoDemo.png)
```
yfBox.tip("info","这里是提示内容",3000)  //3000 指的是3秒后消失
```

### 2.成功提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/successDemo.png)
```
yfBox.tip("success","这里是提示内容",3000) 
```

### 3.失败提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/errorDemo.png)
```
yfBox.tip("error","这里是提示内容",3000) 
```

### 4.警告提示框
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/warningDemo.png)
```
yfBox.tip("warning","这里是提示内容",3000) 
```

# 三、loading加载框
### 1.调出加载框
```
yfBox.load("这里写加载提示文字");  //不填 则默认为 正在加载中...
```
### 2.关闭加载框
```
yfBox.closeLoad();
```

# 四、购物车飞入动画
### 1.单纯的调用购物车飞出的动画
![defaultDemo](https://github.com/ClassName/yfBox/blob/master/images/shopCar.png)
```
yfBox.shopCar(e);        //注意，参数e来自上层函数，如下

btn.click(function(e){  //这里的e必须要出现，以供shopCar函数引用
  yfBox.shopCar(e)
})
```

### 2.直接给指定元素绑定购物车动画
更推荐这种用法，直接给指定元素绑定动画，只需要传入任意多个选择器并自带判断，如果前后值一样或者为空值，不会出现动画
```
yfBox.shopCarInput('选择器一','选择器二','选择器三'...)
yfBox.shopCarInput('.inputone','#inputtwo'...)
```
