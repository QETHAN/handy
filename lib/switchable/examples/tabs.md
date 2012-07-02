<style>
    #demo1 {
        font: 14px/1.5 'Xin Gothic', 'PT Sans', 'Hiragino Sans GB', 'Helvetica Neue', Helvetica, Arial, sans-serif;
        position: relative;
        width: 300px;
        padding-top: 29px;
    }

    #demo1 a {
        text-decoration: none;
    }

    #demo1 .ui-switchable-nav {
        position: absolute;
        left: 20px;
        margin-top: -29px;
        z-index: 99;
    }

    #demo1 .ui-switchable-nav li {
        float: left;
        width: 50px;
        line-height: 21px;
        text-align: center;
        background: #AEC7E5;
        margin-right: 3px;
        padding-top: 8px;
        cursor: pointer;
        list-style: none;
    }

    #demo1 .ui-switchable-nav li.ui-switchable-active {
        background:blue;color:#fff;
    }

    #demo1 .ui-switchable-content {
        position: relative;
        height: 150px;
        padding: 20px;
        border: 1px solid #AEC7E5;
    }
</style>

<div class="s-section">

        <div id="demo1" class="s-demo">
            <ul class="ui-switchable-nav">
                <li>标题 A</li>
                <li>标题 B</li>
                <li>标题 C</li>
                <li>标题 D</li>
            </ul>
            <div class="ui-switchable-content">
                <div style="display: none">
内容 A
<pre>
  - 在当前 trigger 中 mouseover/mouseout, click, focus, 不触发
  - 鼠标快速滑过非当前 trigger, 不触发
  - mouseover 到非当前 trigger, 停留时间到达延迟时，触发
  - click 或 Tab 切换到 trigger, 立即触发
  - switch / switched 事件的触发
</pre>
                </div>
                <div style="display: none;">内容 B</div>
                <div style="display: none;">内容 C</div>
                <div style="display: none;">内容 D</div>
            </div>

        </div>
    </div>

```javascript
    var T, $, tabs;

    seajs.use(['$', 'tabs'], function($, Tabs) {
        T = Tabs;

        tabs = new Tabs({
            element: '#demo1',
            triggers: '.ui-switchable-nav li',
            panels: '.ui-switchable-content div',
            activeIndex: 2,
            effect: 'none'
        });

    });
```