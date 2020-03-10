# Ⅰ Hexo搭建

### 0 常用Hexo命令（参考）

```
初始化hexo：hexo init
启动hexo：hexo s/start
查看hexo命令：hexo c
Commands:
  clean     Remove generated files and cache.
  config    Get or set configurations.
  deploy    Deploy your website.
  generate  Generate static files.
  help      Get help on a command.
  init      Create a new Hexo folder.
  list      List the information of the site
  migrate   Migrate your site from other system to Hexo.
  new       Create a new post.
  publish   Moves a draft post from _drafts to _posts folder.
  render    Render files with renderer plugins.
  server    Start the server.
  version   Display version information.

Global Options:
  --config  Specify config file instead of using _config.yml
  --cwd     Specify the CWD
  --debug   Display all verbose messages in the terminal
  --draft   Display draft posts
  --safe    Disable all plugins and scripts
  --silent  Hide output on console
```



### 1 创建本地blog

1. 安装[Node.js安装及环境配置之Windows篇](https://www.jianshu.com/p/03a76b2e7e00)

2. 设置cnpm淘宝镜像

   ```npm
   npm install -g cnpm --registry=http://registry.npm.taobao.org
   ```

3. 安装hexo

   ```
   cnpm install -g hexo-cli
   ```

4. 正式使用Hexo搭建博客

   ```
   //进入需要创建blog目录的文件夹
   cd D:\GitHub\UBlog
   //新建文件夹
   mkdir HexoBlog
   //进入HexoBlog文件夹
   cd HexoBlog
   ```

   ![1583590582594](D:\GitHub\Notes\WithBeingIT\_static\1583590582594.png)

   5.初始化博客

   ```
   hexo init
   ```

   6.启动/关闭博客

   ```
   hexo s
   ctrl+c
   ```

### 2 管理blog

1. 新建博文

   ```
   hexo n "测试hexo"
   ```

2. 填充内容

   ```
   使用markdown编辑器
   ```

3. 再次启动hexo——测试

### 3 第一次部署Hexo到Github

1. 登录Github

   ![1583595249829](D:\GitHub\Notes\WithBeingIT\_static\1583595249829.png)

2. 新建仓库

   > 用户部署个人博客的github命名必须复核特定要求：
   >
   > 用户昵称.github.io

3. 在*HexoBlog*下安装git deployer插件

   > cnpm install --save hexo-deployer-git

4. 设置_config.yml文件

   ![1583596000476](D:\GitHub\Notes\WithBeingIT\_static\1583596000476.png)

   > 可以使用nodepad++打开

   配置前：

   ![1583596080749](D:\GitHub\Notes\WithBeingIT\_static\1583596080749.png)

   配置后：

   ![1583596375465](D:\GitHub\Notes\WithBeingIT\_static\1583596375465.png)

5. **部署**

   ```
   hexo d
   ```

### 4 修改主题

> 在 Hexo 中有两份主要的配置文件，其名称都是 `_config.yml`。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
>
> 为了描述方便，在说明中，将前者称为 **站点配置文件**， 后者称为 **主题配置文件**。

- 以NexT主题为例

  ```
  $ cd your-hexo-site
  $ git clone https://github.com/iissnan/hexo-theme-next themes/next
  ```

- 启动主题

  ```
  theme: next
  ```

- 部署

  ```
  hexo d
  ```

  