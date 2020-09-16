# nodejs app
- https://devcenter.heroku.com/articles/deploying-nodejs
- https://www.cnblogs.com/lihaozhou/p/4366883.html
- https://stackoverflow.com/questions/53551717/couldnt-find-that-app-when-running-heroku-commands-in-console
- https://www.jianshu.com/p/ef45c59a894b
- https://scotch.io/tutorials/how-to-deploy-a-node-js-app-to-heroku


## github
1. 登录 heroku login
  ```shell
  heroku login
  ```
2. 找到 github 上的项目
  ```shell
  git clone git@github.com:scotch-io/heroku-node
  ```
3. npm install
4. 保证本地可以正常运行项目
5. 登录heroku绑定 github对应的项目
6. git push 会自动 deploy
7. 查看具体的日志： heroku logs --tail

## other
- 创建 heroku app 
  ```shell
  heroku create
  # 或者
  heroku create heroku-node-scotch
  ```
- 重命名
  ```shell
  # 期望的名字: heroku-node
  # heroku自分理处生成的名字: calm-reaches-6216
  heroku apps:rename heroku-node --app calm-reaches-6216
  ```
- 其它平台 deploy到 heroku
  ```shell
  git push heroku master
  ```
- 配置: Procfile
  ```yml
  web: node server.js
  ```
- open打开
  ```shell
  heroku open
  ```


## Using a Current Heroku App
- Download the Heroku Toolbelt
- Login: heroku login
- Add your public key: heroku keys:add
- Pull down your current application heroku git:clone -a app-name
- Make your improvements
- Git add and commit your changes
- Push back to heroku: git push heroku master
