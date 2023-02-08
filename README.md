### 框架
- 前端vue
##### vue前端框架结构
```
├── build                      // 构建相关  
├── mock                       // 项目mock 模拟数据
├── public                     // 公共资源
├── src                        // 源代码
│   ├── api                    // 所有接口请求
│       ├── user.js            // 用户接口
│       ├── board.js           // 主面板接口
│       ├── neo4j.js           // neo4j数据库操作接口
│       ├── product.js         // mysql数据库操作接口
│       ├── askquestion.js     // 问答接口
│   ├── assets                 // 主题 字体等静态资源
│   ├── components             // 全局公用组件
│       ├── d3graph.vue        // 数据节点渲染组件
│       ├── d3graphby.vue      // 数据节点渲染组件
│       ├── d3search.vue       // 数据搜索组件
│       ├── d3searchby.vue     // 数据搜索组件
│       ├── ArticleEditor.vue  // md文件编辑组件
│   ├── directive              // 全局指令
│   ├── filtres                // 全局 filter
│   ├── icons                  // 项目所有 svg icons
│   ├── router                 // 路由
│   ├── store                  // 全局 store管理
│   ├── styles                 // 全局样式
│   ├── utils                  // 全局公用方法
│       ├── get-paper-title.js // 获取页面标题 
│       ├── request.js         // axios请求
│       ├── validate.js        // 判断用户有效性
│   ├── vendor                 // 公用vendor
│   ├── views                  // view
│       ├── dashboard        
│           ├── index.vue      // 控制面板页面
│       ├── login        
│           ├── index.vue      // 登陆页面
│       ├── 2dviewby.vue       //编译原理课程可视化图
│       ├── 2dview.vue         //安全编程语言设计课程可视化图谱界面
│       ├── test       
│           ├── Contactus.vue  // 学习推荐页面
│       ├── AskQuestion.vue    // 智能问答页面
│       ├── 404.vue            // 404页面
│   ├── App.vue                // 入口页面
│   ├── main.js                // 入口 加载组件 初始化等
│   ├── setting.js             // 网址标签
│   └── permission.js          // 权限管理
```
api ：请求服务端接口的配置都在这里，这里逻辑实现是用到了utils里边的封装的request.js，其中在没有正式服务接口的之前是可以直接调用上边mock里的地址，得到模拟的数据请求

在src/settings.js 有一些全局配置，比如title可以修改下系统的名字

- 后端flask
##### flask后端框架结构
```
├── __pycache__                     
├── .idea                    
├── apis                       // 接口
│   ├── __pycache__                   
│   ├── user.py                // 用户蓝图
│   ├── neo4joperation.py      // neo4j蓝图
│   ├── markdown.py            // markdown蓝图
│   ├── product.js             // mysql蓝图
│   ├── askquestion.js         // 问答蓝图
├── configs                    // 相关配置参数
│   ├── __pycache__           
│   ├── config.py              // 数据库配置
│   ├── format.py              // 统一Response返回
├── static                     // 存放静态资源，例如图片、js、css文件等
├── app.py                     // 运行主程序
├── setting.py                 // 路径
└── tfidf.py                   // tfidf搜索代码
```
- 数据库Mysql+Neo4j

### 代码使用
- 前端 
  ```
  cnpm install
  ```
  ```
  cnpm run dev
  ```
- 后端
  pip3安装dbutils、pymysql、py2neo、CORS库
  ```
  python app.py
  ```
### 接口文件
/vue/src/api/...

### 知识图谱构建和知识体系可视化
后端连接neo4j图数据库/flak/apis/neo4joperation.py(增删改查操作)

前端节点渲染/vue/src/components/d3graphby.vue

### 知识推荐与学习路径规划模块设计开发
/vue/src/view/test/contactus.vue

/flask/apis/product.py

### 问答模块设计开发
/vue/src/view/AskQuestion.vue

/flask/apis/product.py
