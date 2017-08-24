# datePicker
a plugin of jquery for picking date
## 使用方法
### 1.导入jquery库文件和datePicker.js
 ```javascript
    <script src="./js/jquery.min.js"></script>
    <script src="./js/datePicker.js"></script>
 ```
### 2.导入样式表
```javascript
    <link rel="stylesheet" type="text/css" href="./css/datePicker.css"></link>
```
### 3.在body中添加如下内容：
```html
    <button class="date-btn">点击显示时间面板</button>
    <!--时间选择器-->
    <div class="datePicker-container">
        <div class="layui-form-pane">
            <div class="layui-input-inline">
                <input class="layui-input start-time" placeholder="选择开始时间" id="LAY_demorange_s">
            </div>

            <div class="layui-input-inline">
                <input class="layui-input end-time" placeholder="选择结束时间" id="LAY_demorange_e">
            </div>
            <div class="date-line">--</div>
            <div class="submit-btn"></div>

            <div class="close-btn"></div>
            <div class="date-container">

            </div>
            <div class="tip">请选择开始时间、结束时间！</div>
        </div>
    </div>

```
### 4.在js中使用插件
```javascript
    $.fn.initPicker('month', '.date-btn', 'click' ,callback)
```
### 5.调用函数参数说明
    $.fn.initPicker(type, dom, eventType, callback)
> **type**: 目前支持'month'和'date'两种类型，month表示时间粒度到月，date表示时间粒度到日。  
> **dom**: 触发时间选择面板显示的dom对象，上面例子中点击class="date-btn"这个按钮时弹出时间选择面板。  
> **eventType**: 表示触发时间选择面板显示的事件类型，上面例子中是点击button，因此设置为'click'，有时候可能要求鼠标移到某个元素上就显示面板。  
> **callback**: 该方法接收两个参数startTime、endTime，表示时间选择完成后的开始时间、结束时间，一般在callback里处理完成时间选择后的后续逻辑
