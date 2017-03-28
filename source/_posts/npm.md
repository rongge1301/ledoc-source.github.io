---
title: npm 组件介绍
date: 2017-03-23 19:11:50
tags:
---
### npm组件文档
<!-- more -->

***

# Dialog 对话框

### 安装
```$xslt
npm install dialog-le
```
### 使用
#### 主题2
![](/images/dialog/1.png) 
```$xslt
Dialog({
    msg: 'test-content', 
    theme: 'theme-2', 
    close:false
})
```

#### 配置参数
![](/images/dialog/2.png)
 ```$xslt
Dialog({
    theme: "theme-2", //默认为theme-1
    msg: '确定放弃吗', //弹窗内容，支持html
    btns: [ //弹窗按钮, 默认为“确认”按钮
        {
            btn_text: '确定',
            btn_class: 'gray-btn', //置灰
            onclick: function(){alert(1)} //可选 默认事件处理为关闭弹窗
        },
        { 
            btn_text: '取消'
        }
    ],
    close: false //可选，是否显示右上角关闭，默认显示 
})
```

#### 主题1
![](/images/dialog/3.png)
```$xslt
Dialog({
    msg: 'test-content', //弹窗内容，支持html
    btns: [ //弹窗按钮, 默认为“确认”按钮
    {
        btn_text: '确定',
        btn_class: '', //可选
        pingback: { //大数据埋点 可选
            'pingback-type': 'click',
            'pingback-action': '0',
            'pingback-category': '5',
            'pingback-props': 'button_name=确定&tar_page=继续支付&ob_ca=收银台首页'
        },

        onclick: function(){alert(1)} //可选 默认事件处理为关闭弹窗
    },
    { 
        btn_text: '取消'
    }
    ],
    close: false //可选，是否显示右上角关闭，默认显示 
})
```

***

##  分享 share-le

### 安装
```$xslt
npm install share-le
```

### 引用
```
var Share = require('share-le');
```
### 使用
```
Share({
                    config: require('./config'),    //配置文件地址
                    eventEle:$('#shareBtn'),        //监听显示分享浮层事件的按钮 
                    shareUrl:shareUrl,              //分享地址 
                    webpageShare:[1],             //h5分享所需的社交平台   0,所有平台 1，微博 
                    appSharePlarform:[0],         //app分享所需的社交平台  0,所有平台 1,微信平台 2，微博 3，qq 4,qq空间 
                    callback:function(){            //分享成功后回调 
                        alert(分享成功);
                    } 
});

```

***

# 提示浮层 tip-le

#### 安装

```$xslt
npm i --save tip-le
```

#### 使用
```$xslt
Tip.success("成功");
Tip.error("失败")
```
