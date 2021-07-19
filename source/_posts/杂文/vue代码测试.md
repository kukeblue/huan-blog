---
title: vue项目测试
tag: 测试
category: 测试
---

# vue项目测试总结

## 测试的种类

测试的种类有3种
1. 单元测试
2. UI测试
3. e2e黑盒测试

## 使用框架Vue TestUtil集成JEST

按我的理解应该是VUE在JEST上对vue-api和dom操作的扩展

## 安装

```
vue add @vue/unit-jest
```
## 配置

主要是配置babel.config.js和jest.config
- 配置babel
```js
module.exports = {
    "presets": [['@vue/app']],
    // 这里为测试环境的配置
    "env": {
        "test": { "presets": [["@babel/preset-env", { "targets": { "node": true } }]] }
    }
}
```
- 配置jest.config

```js
module.exports = {
    preset: '@vue/cli-plugin-unit-jest',
    // 为代码import引入别名
    moduleNameMapper: {
        "^@/(.*)$": "<rootDir>/src/$1"
    }
}
```
## 代码编写

### 代码文件位置

**全局**: `@root/tests/util`目录下，文件以spec.js结尾
**局部**: `@component/helloword/__tests__/helloword.test.js`


### 要测试那些内容

组件单元测试的一个好理念是先假设测试是不必要的，除非被证明是必要的。你可以问自己以下问题：

- 这是业务逻辑的一部分吗？
- 这是直接测试组件的输入和输出吗？
- 这是测试自己的代码，还是第三方代码？


## 待更新





