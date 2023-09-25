# Ziglings

## ⚠️ 注意! Ziglings 已迁移至 Codeberg!

查看我们方便的新 URL: https://ziglings.org

或直接由此访问仓库: https://codeberg.org/ziglings/exercises

***

欢迎来到 Ziglings ！本项目包含一系列微小的破损程序（和一个险恶的惊喜）。
通过修复它们，你将学会如何阅读和编写 [Zig](https://ziglang.org/) 代码。

![ziglings](https://user-images.githubusercontent.com/1458409/109398392-c1069500-790a-11eb-8ed4-7d7d74d32666.jpg)

那些坏掉的程序需要你的帮助！（你还将从邪恶的外星人手中拯救地球，
并帮助一些友好的大象团结在一起，你真是太贴心了）。

这个项目的直接灵感来自于 [Rust](https://www.rust-lang.org/) 语言的
[rustlings](https://github.com/rust-lang/rustlings) 项目。
间接灵感来自 [Ruby Koans](http://rubykoans.com/) 
和 Little LISPer/Little Schemer 系列丛书。

## 目标受众

如果你以前*从未*做过编程，这可能会比较困难。但是特定的编程经验并不是必需的。
尤其是，我们*不*希望你有任何“系统编程”或“系统”级语言（如 C 语言）方面的经验。

每一项练习都是自成一体、自圆其说的。不过，我们鼓励你同时查看这些 Zig 语言资源。
更多细节：

* https://ziglang.org/learn/
* https://ziglearn.org/
* https://ziglang.org/documentation/master/

此外，[Zig 社区](https://github.com/ziglang/zig/wiki/Community) 也非常友好和乐于助人！

## 起步

安装一个 Zig 编译器的 [development build](https://ziglang.org/download/)。
（请参阅下载页面的“master”部分）。

像这样验证 `zig` 的安装和构建编号：

```
$ zig version
0.11.0-dev.4246+xxxxxxxxx
```

用 Git 克隆这个仓库:

```
$ git clone https://ziglings.org
$ cd ziglings.org
```

然后运行 `zig build` 并按照说明开始操作！

```
$ zig build
```

注：Ziglings 的输出是 Zig 编译器未经修改的输出。
Ziglings 的部分目的是让你适应阅读这些内容。

## 关于版本的一个注意事项

Zig 语言正在积极开发中。
为了保证时效性，Ziglings 追踪的是 Zig 编译器的**开发**版本，
而非版本控制的**发行**版本。上一个稳定版本是“0.10.1”，
但 Ziglings 需要一个版本号为“0.11.0”的开发版本，
且其版本号至少与上述版本检查示例中显示的版本号相同。

你很可能会下载到比最小值*大*的版本。

*（对于那些无法轻松更新 Zig 的用户，本仓库中也有社区支持的分支。
目前有一个 v0.8.1 分支。旧版本分支可能有也可能没有所有的练习和/或错误修正。）*

一旦你有一个能与 Ziglings 一起工作的 Zig 编译器构建，它们将持续地协同工作。
但请注意，如果你更新了其中一个，你可能也需要更新另一个。

### 版本变动

Version-0.11.0-dev.4246+71dfce31b
* *2023-06-26* zig 0.11.0-dev.4246 - changes in compile step (now it can be null)
* *2023-06-26* zig 0.11.0-dev.3853 - removal of destination type from all cast builtins
* *2023-06-20* zig 0.11.0-dev.3747 - `@enumToInt` is now `@intFromEnum` and `@intToFloat` is now `@floatFromInt`
* *2023-05-25* zig 0.11.0-dev.3295 - `std.debug.TTY` is now `std.io.tty`
* *2023-04-30* zig 0.11.0-dev.2704 - use of the new `std.Build.ExecutableOptions.link_libc` field
* *2023-04-12* zig 0.11.0-dev.2560 - changes in `std.Build` - remove run() and install()
* *2023-04-07* zig 0.11.0-dev.2401 - fixes of the new build system - see [#212](https://github.com/ratfactor/ziglings/pull/212)
* *2023-02-21* zig 0.11.0-dev.2157 - changes in `build system` - new: parallel processing of the build steps
* *2023-02-21* zig 0.11.0-dev.1711 - changes in `for loops` - new: Multi-Object For-Loops + Struct-of-Arrays
* *2023-02-12* zig 0.11.0-dev.1638 - changes in `std.Build` cache_root now returns a directory struct
* *2023-02-04* zig 0.11.0-dev.1568 - changes in `std.Build` (combine `std.build` and `std.build.Builder` into `std.Build`)
* *2023-01-14* zig 0.11.0-dev.1302 - changes in `@addWithOverflow` (now returns a tuple) and `@typeInfo`; temporary disabled async functionality
* *2022-09-09* zig 0.10.0-dev.3978 - change in `NativeTargetInfo.detect` in build
* *2022-09-06* zig 0.10.0-dev.3880 - Ex 074 correctly fails again: comptime array len
* *2022-08-29* zig 0.10.0-dev.3685 - `@typeName()` output change, stage1 req. for async
* *2022-07-31* zig 0.10.0-dev.3385 - std lib string `fmt()` option changes
* *2022-03-19* zig 0.10.0-dev.1427 - method for getting sentinel of type changed
* *2021-12-20* zig 0.9.0-dev.2025 - `c_void` is now `anyopaque`
* *2021-06-14* zig 0.9.0-dev.137  - std.build.Id `.Custom` is now `.custom`
* *2021-04-21* zig 0.8.0-dev.1983 - std.fmt.format() `any` format string required
* *2021-02-12* zig 0.8.0-dev.1065 - std.fmt.format() `s` (string) format string required

## 高级用法

只检查一项练习也很方便：

```
zig build -Dn=19
```

你也可以不检查正确性而直接运行：

```
zig build -Dn=19 test
```

或者完全跳过构建系统，直接与编译器交互，如果你喜欢做这种事的话：

```
zig run exercises/001_hello.zig
```

召唤所有的巫师：想要为调试准备一个可执行文件，要通过以下命令将其安装到 zig-cache/bin 中：

```
zig build -Dn=19 install
```

想要获取一个所有可能的选项的列表，运行：

```
zig build -Dn=19 -l

  install          安装 019_functions2.zig 到前缀路径
  uninstall        从前缀路径卸载 019_functions2.zig
  test             运行 019_functions2.zig 而无需检查输出
  ...
```

## 覆盖范围

Ziglings 的主要目标是涵盖核心 Zig 语言。

如果能将标准库也包括在内就更好了，但目前这还具有挑战性，
因为 stdlib 的发展速度甚至比核心语言还要快（这还不算什么！）。
不仅 stdlib 的覆盖范围会迅速变化，有些练习甚至可能完全不再相关。

尽管如此，仍有一些 stdlib 功能可能会继续存在，
或者理解它们是如此重要，以至于它们值得额外的努力来保持最新趋势。

很明显，Ziglings 中没有大量的字符串操作练习。
这是因为 Zig 本身在很大程度上避免处理字符串。
希望将来能有明显的方法解决这个问题。
Ziglings 团队热爱字符串！

Zig 核心语言

* [x] Hello world (main 函数需要是 public 的)
* [x] 导入标准库
* [x] 赋值
* [x] 数组
* [x] 字符串
* [x] If 分支
* [x] While 循环
* [x] For 循环
* [x] 函数
* [x] 错误 (error/try/catch/if-else-err)
* [x] Defer (and errdefer)
* [x] Switch 分支
* [x] Unreachable
* [x] 枚举
* [x] 结构体
* [x] 指针
* [x] 可选值
* [x] 结构体方法
* [x] 切片
* [x] 多项指针
* [x] 联合体
* [x] 数值类型 (整数, 浮点数)
* [x] 带标签的块和循环
* [x] 循环表达式
* [x] 内置函数
* [x] 行内循环
* [x] 编译期
* [x] 末端标记
* [x] 带引号的标识符 @""
* [x] 匿名结构体/元组/列表
* [ ] 异步 <--- 黑着脸等待上游 Zig 的更新
* [X] 接口
* [X] 位运算
* [X] 与 C 语言一起工作

Zig 标准库

* [X] 字符串格式化
* [X] 测试
* [X] 分词

## 贡献

贡献是非常受欢迎的！我写这个的目的是自学，
并创建我所希望的学习资源。还有大量的改进空间：

* 解释说明的措辞
* Zig 的习惯用法
* 额外的练习

请查阅本仓库中的 [CONTRIBUTING](https://github.com/ratfactor/ziglings/blob/main/CONTRIBUTING.md) 来获取完整的细节。
