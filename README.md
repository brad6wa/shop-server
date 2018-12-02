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
#### 本地环境配置
  - 初始化数据库 mydb.sql
  - 修改后台项目shop2-server的数据库配置信息
    + shop2-server\config\default.json
      -db_config.database = 数据库名称()
      -db-config.user = root
      -db-congig.password = ''
  - 修改前端项目()的配置文件接口
    +itcast\src\api\api.js
      - baseURL = 'http://localhost:8888/api/private/v1/'
  - 启动后台项目: 在项目根目录执行 node app.js
  - 启动前端项目: 在项目根目录执行 npm run dev