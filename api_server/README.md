#### 项目整体文件说明
- `config` 配置文件目录
  - `default.json` 默认配置文件（其中包含数据库配置，jwt配置）
- `dao` 数据访问层，存放对数据库的增删改查操作
  - `DAO.js` 提供的公共访问数据库的方法
- `models` 存放具体数据库 ORM 模型文件
- `modules` 当前项目模块
  - `authorization.js` API权限验证模块
  - `database.js` 数据库模块（数据库加载基于 nodejs-orm2 库加载）
  - `passport.js` 基于 passport 模块的登录搭建
  - `resextra.js` API 统一返回结果接口
- `node_modules` 项目依赖的第三方模块
- `routes` 统一路由
  - `api` 提供 api 接口
  - `mapp` 提供移动APP界面
  - `mweb` 提供移动web站点
- `services` 服务层，业务逻辑代码在这一层编写，通过不同的接口获取的数据转换成统一的前端所需要的数据
- `app.js` 主项目入口文件
- `package.json` 项目配置文件



- 部署步骤
- 1. 创建数据库 名称任意 比如  mydb  当做该项目的数据库
- 2. 将db目录下的sql文件 导入创建的数据库 自动创建表和插入数据 可直接将sql文件直接拖动到navicate的数据库名称上 快捷完成
- 3. 使用txt或notepad++ 打开config目录的 default.json 文件 db_config 就是配置数据库的信息 填入项目数据库信息
- 4. 本地电脑安装node.js   将nodejs目录添加到环境变量 打开cmd 输入 node -v 可查看node版本 即安装成功  安装node.js 会自动安装npm命令
- 5. 在项目目录下打开cmd命令行 输入npm install   自动安装项目所需的依赖
- 6. 启动项目 在项目目录下打开cmd命令行 输入node 空一格 然后输入app.js 然后按回车键 没有报错 说明项目启动成功
