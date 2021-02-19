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
其中 **Header** 必填，**Body** 与 **Footer** 选填。

不管是哪一个部分，任何一行都不得超过100个字符。

## Header
**Header** 部分只有一行，包括三个字段：**type**（必需）、**scope**（可选）和 **subject**（必需）

* type

    type 用于说明 commit 的类别，只允许使用下面7个标识

    1. feat ：新功能（feature）
    2. fix ：修补bug
    3. docs ：文档（documentation）
    4. style ： 格式（不影响代码运行的变动）
    5. refactor ：重构（即不是新增功能，也不是修改bug的代码变动）
    6. perf ：性能、体验优化
    7. test ：增加、更新测试
    8. chore ：构建过程或辅助工具的变动
    9. build ：构建变动
    10. ci ：集成变动
    11. revert ： 回滚某个提交
    
如果 **type** 为 **feat** 和 **fix**，则该 **commit** 将肯定出现在 Change log 之中。其他情况由你决定，要不要放入 Change log，建议是不要。

* scope

    **scope** 用于说明 **commit** 影响的范围，比如数据层、控制层、视图层等等，视项目不同而不同。

* subject

    **subject** 是 **commit** 目的的简短描述，不超过50个字符。

1. 以动词开头，使用第一人称现在时，比如 change，而不是 changed 或 changes
2. 第一个字母小写
3. 结尾不加句号

## Body
**Body** 部分是对本次 **commit** 的详细描述，可以分成多行。


## Footer
**Footer** 部分只用于两种情况。
>1. 不兼容变动<br>
如果当前代码与上一个版本不兼容，则 Footer 部分以BREAKING CHANGE开头，后面是对变动的描述、以及变动理由和迁移方法。

>2. 关闭 Issue<br>
如果当前 commit 针对某个issue，那么可以在 Footer 部分关闭这个 issue 。
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
featurepush-notification v{version-code}
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
## GitHub 缩写
* PR: Pull Request. 拉取请求，给其他项目提交代码。
* LGTM: Looks Good To Me. 朕知道了 代码已经过 review，可以合并。
* SGTM: Sounds Good To Me. 和上面那句意思差不多，也是已经通过了 review 的意思。
* WIP: Work In Progress. 传说中提 PR 的最佳实践是，如果你有个改动很大的 PR，可以在写了一部分的情况下先提交，但是在标题里写上 * WIP，以告诉项目维护者这个功能还未完成，方便维护者提前 review 部分提交的代码。
* PTAL: Please Take A Look. 你来瞅瞅？用来提示别人来看一下。
* TBR: To Be Reviewed. 提示维护者进行 review。
* TL;DR: Too Long; Didn't Read. 太长懒得看。也有很多文档在做简略描述之前会写这么一句。
* TBD: To Be Done(or Defined/Discussed/Decided/Determined). 根据语境不同意义有所区别，但一般都是还没搞定的意思。

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