<style>
    * {
        margin: 0;
        padding: 0;
    }

    li {
        list-style: none;
    }

    li a {
        text-decoration: none;
    }

    h2 { margin: 30px 0 10px; font-size: 17px; }
    .loading { background: #EBF5FA url(assets/loading.gif) no-repeat 50% 50%; }

    p.code-switch { color: #09f; cursor: pointer; margin-top: 10px; }
    pre.code {
        color: #444;
        cursor: auto;
        border-left: 2px solid #7F96AA;
        margin-top: 5px;
        padding: 0 10px 20px 10px;
        font-size: 14px;
    }
</style>

<h2>Accordion - 手风琴</h2>
<style>
    #accordion1 {width:200px;border:1px solid #ccc;}
    #accordion1 .ui-switchable-trigger{padding:3px 10px;cursor:pointer;border-bottom:1px solid #ddd;background:#f3f3f3;overflow:hidden; height: 18px;}
    #accordion1 .ui-switchable-trigger h3{float: left; width: 100px; margin-left: 5px; }
    #accordion1 .ui-switchable-panel{padding:3px 10px;border-bottom:1px solid #ddd;}
    #accordion1 .ui-icon{float:left;width:12px;height:12px;overflow:hidden;margin-top:2px;font-size:0;vertical-align:middle;background:url(assets/accordion-sprite.png) no-repeat 0 0;}
    #accordion1 .ui-switchable-active .ui-icon{background-position:-20px 0;}
    #accordion1 .last-trigger { border-bottom-width: 0 }
    #accordion1 .ui-switchable-active { border-bottom-width: 1px }
    #accordion1 .last-panel { border-bottom: none }
</style>
<div id="accordion1" class="section" data-widget="accordion">
    <div class="ui-switchable-trigger ui-switchable-active"><i class="ui-icon"></i><h3>标题A</h3></div>
    <div class="ui-switchable-panel">
        1、支持鼠标滑过和点击触点两种方式<br/>
        2、支持同时展开多个面板
    </div>
    <div class="ui-switchable-trigger"><i class="ui-icon"></i><h3>标题B</h3></div>
    <div class="ui-switchable-panel" style="display:none;">内容B<br/>内容B<br/>内容B</div>
    <div class="ui-switchable-trigger"><i class="ui-icon"></i><h3>标题C</h3></div>
    <div class="ui-switchable-panel" style="display:none;">内容C<br/>内容C<br/>内容C<br/>内容C<br/>内容C</div>
    <div class="ui-switchable-trigger last-trigger"><i class="ui-icon"></i><h3>标题D</h3></div>
    <div class="ui-switchable-panel last-panel" style="display:none;">内容D<br/>内容D<br/>内容D</div>
</div>

```javascript
seajs.use(['$', 'accordion'], function($, Accordion) {
    new Accordion({
        element: '#accordion1',
        triggers: '#accordion1 .ui-switchable-trigger' ,
        panels: '.ui-switchable-panel'
    });
});
```