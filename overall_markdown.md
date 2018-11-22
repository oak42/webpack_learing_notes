深入浅出Webpack [2017]


contents

前言

1 入门
1.1 前端的发展
1.1.1 模块化
1.1.2 新框架
1.1.3 新语言
1.2 常见的构建工具及对比
1.2.1 Npm Script
1.2.2 Grunt
1.2.3 Gulp
1.2.4 Fis3
1.2.5 Webpack
1.2.6 Rollup
1.2.7 为什么选择Webpack
1.3 安装Webpack
1.3.1 安装Webpack到本项目
1.3.2 安装Webpack到全局
1.3.3 使用Webpack
1.4 使用Loader
1.5 使用Plugin
1.6 使用DevServer
1.6.1 实时预览
1.6.2 模块热替换
1.6.3 支持Source Map
1.7 核心概念

2 配置
2.1 Entry
2.1.1 context
2.1.2 Entry类型
2.1.3 Chunk的名称
2.1.4 配置动态Entry
2.2 Output
2.2.1 filename
2.2.2 chunkFileName
2.2.3 path
2.2.4 publicPath
2.2.5 crossOriginLoading
2.2.6 libraryTarget和library
2.2.7 libraryExport
2.3 Module
2.3.1 配置Loader
2.3.2 noParse
2.3.3 parser
2.4 Resolve
2.4.1 alias
2.4.2 mainFields
2.4.3 extensions
2.4.4 modules
2.4.5 descriptionFiles
2.4.6 enforceExtension
2.4.7 enforceModuleExtension
2.5 Plugin
2.6 DevServer
2.6.1 hot
2.6.2 inline
2.6.3 historyApiFallback
2.6.4 contentBase
2.6.5 headers
2.6.6 host
2.6.7 port
2.6.8 allowedHosts
2.6.9 disableHostCheck
2.6.10 https
2.6.11 clientLogLevel
2.6.12 compress
2.6.13 open
2.7 其他配置项
2.7.1 Target
2.7.2 Devtool
2.7.3 Watch和WatchOptions
2.7.4 Externals
2.7.5 ResolveLoader
2.8 整体配置结构
2.9 多种配置类型
2.9.1 导出一个Function
2.9.2 导出一个返回Promise的函数
2.9.3 导出多份配置
2.10 总结

3 实战 
3.1 使用ES6语言
3.1.1 认识Babel
3.1.2 接入Babel
3.2 使用TypeScript语言
3.2.1 认识TypeScript
3.2.2 减少代码冗余
3.2.3 集成Webpack
3.3 使用Flow检查器
3.3.1 认识Flow
3.3.2 使用Flow
3.3.3 集成Webpack
3.4 使用SCSS语言
3.4.1 认识SCSS
3.4.2 接入Webpack
3.5 使用PostCSS
3.5.1 认识PostCSS
3.5.2 接入Webpack
3.6 使用React框架
3.6.1 React的语法特征
3.6.2 React与Babel
3.6.3 React与TypeScript
3.7 使用Vue框架
3.7.1 认识Vue
3.7.2 接入Webpack
3.7.3 使用TypeScript编写Vue应用
3.8 使用Angular2框架
3.8.1 认识Angular2
3.8.2 接入Webpack
3.9 为单页应用生成HTML
3.9.1 引入问题
3.9.2 解决方案
3.10 管理多个单页应用
3.10.1 引入问题
3.10.2 解决方案
3.11 构建同构应用
3.11.1 认识同构应用
3.11.2 解决方案
3.12 构建Electron应用
3.12.1 认识Electron
3.12.2 接入Webpack
3.13 构建Npm模块
3.13.1 认识Npm
3.13.2 抛出问题
3.13.3 使用Webpack构建Npm模块
3.13.4 发布到Npm
3.14 构建离线应用
3.14.1 认识离线应用
3.14.2 认识Service Workers
3.14.3 接入Webpack
3.14.4 验证结果
3.15 搭配Npm Script
3.15.1 认识Npm Script
3.15.2 Webpack为什幺需要Npm Script
3.16 检查代码
3.16.1 代码检查具体是做什么
3.16.2 怎么做代码检查
3.16.3 结合Webpack检查代码
3.17 通过Node.js API启动Webpack
3.17.1 安装和使用Webpack模块
3.17.2 以监听模式运行
3.18 使用Webpack Dev Middleware
3.18.1 Webpack Dev Middleware支持的配置项
3.18.2 Webpack Dev Middleware与模块热替换
3.19 加载图片
3.19.1 使用file-loader
3.19.2 使用url-loader
3.20 加载SVG
3.20.1 使用raw-loader
3.20.2 使用svg-inline-loader
3.21 加载Source Map
3.21.1 该如何选择
3.21.2 加载现有的Source Map
3.22 实战总结

4 优化
4.1 缩小文件的搜索范围
4.1.1 优化loader配置
4.1.2 优化resolve.modules配置
4.1.3 优化resolve.mainFields配置
4.1.4 优化resolve.alias配置
4.1.5 优化resolve.extension配置
4.1.6 优化module.noParse配置
4.2 使用DLLPlugin
4.2.1 认识DLL
4.2.2 接入Webpack
4.3 使用HappyPack
4.3.1 使用HappyPack
4.3.2 HappyPack的原理
4.4 使用ParallelUglifyPlugin
4.5 使用自动刷新
4.5.1 文件监听
4.5.2 自动刷新浏览器
4.6 开启模块热替换
4.6.1 模块热替换的原理
4.6.2 优化模块热替换
4.7 区分环境
4.7.1 为什么需要区分环境
4.7.2 如何区分环境
4.7.3 结合UglifyJS
4.7.4 第三方库中的环境区分
4.8 压缩代码
4.8.1 压缩JavaScript
4.8.2 压缩ES6
4.8.3 压缩CSS
4.9 CDN加速
4.9.1 什么是CDN
4.9.2 接入CDN
4.9.3 用Webpack实现CDN的接入
4.10 使用Tree Shaking
4.10.1 认识Tree Shaking
4.10.2 接入Tree Shaking
4.11 提取公共代码
4.11.1 为什么需要提取公共代码
4.11.2 如何提取公共代码
4.11.3 如何通过Webpack提取公共代码
4.12 分割代码以按需加载
4.12.1 为什么需要按需加载
4.12.2 如何使用按需加载
4.12.3 用Webpack实现按需加载
4.12.4 按需加载与ReactRouter
4.13 使用Prepack
4.13.1 认识Prepack
4.13.2 接入Webpack
4.14 开启Scope Hoisting
4.14.1 认识Scope Hoisting
4.14.2 使用Scope Hoisting
4.15 输出分析
4.15.1 官方的可视化分析工具
4.15.2 webpack-bundle-analyzer
4.16 优化总结

5 原理
5.1 工作原理概括
5.1.1 基本概念
5.1.2 流程概括
5.1.3 流程细节
5.2 输出文件分析
5.3 编写Loader
5.3.1 Loader的职责
5.3.2 Loader基础
5.3.3 Loader进阶
5.3.4 其他Loader API
5.3.5 加载本地Loader
5.3.6 实战
5.4 编写Plugin
5.4.1 Compiler和Compilation
5.4.2 事件流
5.4.3 常用的API
5.4.4 实战
5.5 调试Webpack
5.6 原理总结

A 常用的Loader
B 常用的Plugin
C Webpack的其他学习资源
