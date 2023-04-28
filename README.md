# 前端导航

## 经验与教训
### 写项目时思路
1. 定一个目标，实现它
    目标要小且具体，方便在没有思路时行动
2. 没有完美，做到看不出BUG
    总会有站在不同角度产生的完美方案   
3. 做到后面需要修改前面的内容，不要灰心
    写完再改，这是很正常的事情

### 写CSS时犯的错误
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

### `{margin:0 auto;}`的写法不推荐
```
{
    marging-left: auto;
    marging-right: auto;
}
```