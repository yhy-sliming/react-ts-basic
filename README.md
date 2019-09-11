# react-ts-basic
project with react+typescript for publish to npm 

### basic
**typescript:**

**prettier:** 按照一定的规则来美化你的代码，可配合**eslint/tslint**等一起使用，效果更佳

**tslint:** typescript代码校验规则

**tslint-config-prettier:** 使prettier搭配tslint一起使用


## 设置 git 提交的校验钩子
***
安装
    
    
pre-commit可以自动在.git/下生成 pre-commit 脚本
安装完毕后在package.json中进行配置：

``` json
"pre-commit": [
    "lint"
  ]
```
此处的lint命令就是scripts的lint，再次提交 git commit 会先执行 scripts 下的 {"lint": "tslint -p tsconfig.json"}进行 tslint 代码检查

如果想忽略代码检查可以执行git commit -m'描述' --no-verify（或者-n）进行直接提交


### 目录信息
doc/ 目录存放的是写的文档
example/ 目录是本地开始测试时候要用到的
lib/ 目录是编译tsx文件后将要发布到npm的目录 (tsconfig.json中需要配置outDir为该目录)
src/ 目录是该插件具体开发的目录
src/component 目录是该插件目录
src/types 目录是开发过程中定义类型的目录
