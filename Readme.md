这是我的vue练习项目内容。我会将我的练习代码，及心得放在这里。
This is the content of my vue practice project. I will put my practice code and experience here.
# myFirstVUEPage.html
这是我的第一个练习，本文件主要是熟悉vue是基本格式。
This is my first exercise, this file is mainly familiar with vue is the basic format.
```html
 <div id="app">
        {{10+20}}
        {{ message }}
        {{ myhtml }}
         <!-- 指令 -->
    <div v-html="myhtml"></div>
    <div v-show="isShow">动态显示隐藏</div>
    <div v-if="isCreated">动态创建删除</div>
    </div>   
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="lib/vue.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                message: 'Hello Vue!',
                isShow:true,//这种是隐藏
                isCreated:true,//这种如果为false，则直接不存在
                myhtml:"<a href='http://www.baidu.com'>sss</a>"
            }
        })
    </script>
```
# vue-class绑定.html
在本文件中，主要实现了class的绑定，及样式切换。
In this document, the main implementation of class binding, and style switching.
```html
<script type="text/javascript" src="lib/vue.js"></script>
    <style>
        
        .red{
            background: red;
        }
        .yello{
            background: yellow;
        }
    </style>
</head>

<body>
    <div id="box">
        <button @click="handleClick()">22</button>
        <div :class="isActive?'red':'yello'">我是动态绑定class-三目写法</div>
    </div>
    <script>
        new Vue({
            el:"#box",
            data:{
                isActive:true
            },
            methods:{
                handleClick(){
                this.isActive=!this.isActive
            }}
        })
    </script>
</body>

```