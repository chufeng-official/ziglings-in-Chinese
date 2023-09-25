# 贡献

阅读本文档，即表示您已进入 Ziglings 维护的精英殿堂！

## Ziglings 的受众

Ziglings 适用于各种经验水平的程序员。无需掌握特定的语言知识。
任何人只要能安装当前的 Zig 快照、设置一份 Ziglings 副本，
并了解常用的语言构件（分支、循环和函数），就可以使用 Ziglings。

Ziglings 的目的是完全自成一体。
如果您无法根据目前从 Ziglings 中收集到的信息解决某个练习，
那么该练习可能还需要一些额外的工作。请提交一个 issue ！

如果一个示例与描述不符或有不清楚的地方，请提交一个 issue ！

## 拼写/语法

如果你看到了任何错别字，请提交一个 issue ……或者发起一个 pull request ！

错误不嫌小。Ziglings 必须是完美的。:-)

## 创意

如果您有关于新课程或改进 Ziglings 的创意，请毫不犹豫地提交一个 issue。

请随时提交新的练习，但请理解，
如果我们认为这些练习因某种原因不合适，
它们可能会被大量修改或完全拒绝。

## 平台和 Zig 版本

由于它使用的是 Zig 构建系统，因此只要 Zig 能运行的地方，Ziglings 应该就能运行。

由于 Ziglings 是 Zig 语言学习资源，因此它可以从官方网站下载页面跟踪 Zig 当前的开发快照。

如果您在 Ziglings 中遇到因 Zig 最新开发版本中的破坏性更改而导致的错误，
这就是 Ziglings 中的一个新 bug。请提交一个 issue ……或发起 pull request！

## 格式化

所有的练习都应该遵守 `zig fmt`。我经常忘记去做这件事。

## Pull Request 工作流

Ziglings 使用“标准的” Github 工作流作为向导通过 Web 接口，具体为：

* 派生这个仓库
* 从 `main` 分支创建一个分支以支持你的工作：
      `git checkout -b my-branch`
* 进行修改，提交它们
* 当你的修改准备好送交审核时，推送你的分支：
      `git push origin my-branch`
* 从你的分支创建一个到  `ziglings/main` 分支的 pull request
* 你忠实的 Ziglings 维护者将尽快查看你的请求（2022年5月到7月期间就不说了，哈哈）
* 一旦更改通过审核，您的请求将被合并，永恒的 Ziglings 贡献者的荣耀将属于你！

## 秘密

如果你想窥探其中的秘密，请查看 `patches/` 目录。
