## angular-message
### 版本
version 1.0.0
### 说明
一个基于bootstrap、angular的消息提示，目前支持的API有：  
- **popMessage** 触发弹出消息，主要参数配置有`message(消息文本)`,`type(消息类型,1成功,2错误,3加载,4警告)`，`mask(遮罩层)`，`time(消息显示存活时间)`  
- **removeMessage** 移除消息  
- **slideUpMessage** 移除并动画弹回消息

### 依赖
- jquery
- angular 
- font-awesome  

### 使用方式  

**html代码**  
```html
<body ng-app="app" ng-controller="ctrl">
</body>
```

**angular代码**  
```javascript
var app = angular.module("app",["ui.message"]);
    app.controller("ctrl",["$messageFactory",function($messageFactory){
        $messageFactory.popMessage({
            message: "加载中",
            type:2,
            mask: true,
            time:2000
        });
    }]);
```
### future
根据业务需求，自己扩展想要的功能。