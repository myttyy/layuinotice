# 基于layui的notice通知控件

#### 项目介绍

##### 更新日志
-  2019-03-26 
 - 重构V2版本，如需使用V1版请查看v1分支
 - 新增多种位置选择
 - 优化同时显示多条通知
 - **css代码初始化js载入，不独立文件css文件。**

##### 更新日志
- 2018年9月18日
 - **感谢layui社区成员@Thans修改了本插件**
 - 优化显示位置，改到右侧。（@Thans）
 - 可以同时显示多条通知（@Thans）
 - css代码初始化载入，不独立文件。（@Thans）
 - 在Thans修改版本上增加桌面提醒

基于layui的notice通知控件,算是对layer的一个小扩展

列示：
![](./images/2.png)

#### 使用说明

1. 配置layui扩展

```javascript
    layui.config({
        base: './../dist/'
    });
```

3. 调用API

```javascript
layui.use(['notice'], function () {
    var notice = layui.notice; // 允许别名 toastr
        
        // 初始化配置，同一样式只需要配置一次，非必须初始化，有默认配置
        notice.options = {
            closeButton:true,//显示关闭按钮
            debug:false,//启用debug
            positionClass:"toast-top-right",//弹出的位置,
            showDuration:"300",//显示的时间
            hideDuration:"1000",//消失的时间
            timeOut:"2000",//停留的时间
            extendedTimeOut:"1000",//控制时间
            showEasing:"swing",//显示时的动画缓冲方式
            hideEasing:"linear",//消失时的动画缓冲方式
            iconClass: 'toast-info', // 自定义图标，有内置，如不需要则传空 支持layui内置图标/自定义iconfont类名
            onclick: null, // 点击关闭回调
        };


        notice.warning("成功");
        notice.info("提示信息：毛都没有...");
        notice.error("大佬，我咋知道怎么肥四！");
        notice.success("大佬，我咋知道怎么肥四！");
       
        // 手动移除notice 或者使用 removeToast
        notice.hideToast()
        
});
```
4. positionClass属性可选值：
- toast-top-center
- toast-bottom-center
- toast-top-full-width
- toast-bottom-full-width
- toast-top-left
- toast-top-right
- toast-bottom-right 
- toast-bottom-left

5. 其他配置项看源码吧，不是很难理解的

5. 支持方法

```javascript
layui.use(['notice'], function () {
    // 警告提示
    notice.warning("提示内容");
    // 正常提示
    notice.info("提示内容");
    // 异常提示
    notice.error("提示内容");
    // 
     notice.success("提示内容");
});
```



#### 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request



