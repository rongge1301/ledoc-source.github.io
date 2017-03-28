---
title: modules组件模块
date: 2017-03-28 16:44:42
tags:
categories: "项目"
---

modules组件文档

<!-- more -->
****
# 用户系统五步组件

#### 引用组件
```
var FiveStep = require("jspath/modules/fivestep/index");
```

#### 使用
先初始化
```
FiveStep.init(data);
```

检查用户信息
```
/**
 * 验证是否完成第stepnum步，并且弹框提示
 *
 * @param {number} 数字.
 *
 * 返回boolean
 */
FiveStep.check(5);  //1:是否登录,2:是否实名, 3:是否绑卡, 4: 是否设置交易密码, 5: 是否完成分先测评
```

检查用户设置到第几步
```
FiveStep.getCurrentStep();  //返回数字
```
验证第stepnum是否完成
```
FiveStep.checkStep(stepnum)
```

***

# CountDown (倒计时)

引入
```
var CountDown = require("jspath/modules/countdown/index");
```
使用
```
CountDown({
    'ele':$("xxx"), //显示倒计时的dom元素
    'formate':'dd天hh时mm分ss秒', //格式 如要只显示秒 formate="ss秒"
    'remain_second': res.remain_second, //剩余秒数
    'onOver': function(){ //倒计时结束
    }
});
```