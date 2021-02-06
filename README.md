# Commit message 和 Change log
> 良好的commit message能大大提高代码维护的效率，不仅可以让我们清晰的了解所提交代码的目的，更能方便快速的查找过滤改动信息，还有利于日后直接从commit生成Change log
## 格式
```
<!-- header -->
<type>(<scope>): <subject>
<!-- 空一行 -->
<body>
<!-- 空一行 -->
<footer>
```
## 实例
```
build(package.json): 修改typescript版本到3.4.2

为了支持“项目引用”等新特性，需要修改typescript版本到3.x

BREAKING CHANGE：随着typescript版本的更新，项目中使用的escapeIdentifier方法将不再支持。

PR Close #1
```
## 参考
----
[git commit 规范](https://xrkffgg.js.cool/Knotes/standard/#_1-2-git-commit-%E8%A7%84%E8%8C%83)

[Commit message 和 Change log 编写指南](https://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)
<br/>
<br/>

# branch与tags
> tag是静态的，branch要向前走；tag就像是一个里程碑一个标志一个点，branch是一个新的征程一条线；稳定版本备份用tag，新功能多人开发用branch（开发完成后merge到master）。
## 格式
```
版本分支: 
version/{version-code-without-build-code}
实例：
version/1.2.3

需求分支: feature/{feature-name}
实例：
featurepush-notification
feature/login

个人分支: 
person/{developer-fullname}/{what-for}
实例：
person/gongbenwuzang/network-cache
person/jimgreen/bugfix-12345-crash

tag: 
v{version-code}
实例：
v1.2.3

特殊分支: 
special/{what-for}
实例：
special/blind-apple
special/temp/version/1.0.2
```
## 参考
----
[Git分支管理规范](https://blog.csdn.net/hursing/article/details/78789204)
<br/>
<br/>

# Pull requests
>拉取请求Pull Request是 Github 上的一个工具，允许软件开发人员讨论并提出对项目的主要代码库的更改，这些更改稍后可以部署给所有用户看到。这个功能创建于 2008 年 2 月，其目的是在接受（合并）之前，对某人的建议进行更改，然后在部署到生产环境中，供最终用户看到这种变化。
## 参考
[如何使用Pull request](https://blog.csdn.net/qq_39375237/article/details/109832043)

[GitHub 缩写](https://xrkffgg.js.cool/Knotes/standard/#_1-3-github-%E7%BC%A9%E5%86%99)
<br/>
<br/>

# Issues
> Issues是一种伟大的工作方式，它用于对项目进行跟踪、增强和排错。
## 参考
[掌握 Issues](https://blog.csdn.net/qq_38970783/article/details/90381347)
<br/>
<br/>

# Project
> Project 提供了真正的管理 issue 的能力；
## 参考
[使用Github Project做 TODO管理](https://blog.csdn.net/euphorias/article/details/105509508)
<br/>
<br/>

# Actions
> GitHub Actions 是 GitHub 官方推出的持续集成/部署模块服务（CI/CD）。
## 参考
[利用GitHub Actions自动化打包部署服务器](https://blog.csdn.net/qq_35374262/article/details/108127204)