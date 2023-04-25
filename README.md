# 前端导航

## 经验与教训
### 写CSS时范的错误
```
.siteList .addButton 
.siteList.addButton 
```
上方代码 完全是两个选择器，写的时候 要看仔细

### 写HTML的时候 ，把多个元素放置在 一个li里面，不利于布局
```
<li>
    <div class="site">
        <div class="logo">C</div>
        <div class="link">clicli.com</div>
    </div>
    <div class="site">
        <div class="logo">C</div>
        <div class="link">clicli.com</div>
    </div>
    <div class="site">
        <div class="logo">C</div>
        <div class="link">clicli.com</div>
    </div>
</li>
```
建议写成下面
```
<li>
    <div class="site">
        <div class="logo">C</div>
        <div class="link">clicli.com</div>
    </div>
</li>
<li>
    <div class="site">
        <div class="logo">B</div>
        <div class="link">bilibili.com</div>
    </div>
</li>
<li>
    <div class="addButton">
        新增网站
    </div>
</li>
```
### 容器的高度尽量不要写
不要写怎么确定高度？
1. 由内容确定，内容把 容器撑起来
2. 使用 padding
3. 实在没有办法 写hight,指定高度