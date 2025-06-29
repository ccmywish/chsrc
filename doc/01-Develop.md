<!-- -----------------------------------------------------------
 ! SPDX-License-Identifier: GFDL-1.3-or-later
 ! -------------------------------------------------------------
 ! Doc Type      : Markdown
 ! Doc Name      : 01-Develop.md
 ! Doc Authors   : Aoran Zeng <ccmywish@qq.com>
 ! Contributors  :  Nul None  <nul@none.org>
 !               |
 ! Created On    : <2024-12-27>
 ! Last Modified : <2025-06-19>
 ! ---------------------------------------------------------- -->

# 开发

## 开发环境

请安装好：

  1. `GCC` 或 `Clang`
  2. [just] 或 `make`
  3. `curl`

**我推荐你使用 VS Code 开发，你可以在一分钟内成功编译、运行和 Debug `chsrc`**

  1. `Ctrl-Shift-B` 直接构建
  2. `F5` 直接开始 Debug

<br>


## 准备

```bash
# 请务必使用 dev 分支开发
$ git clone https://gitee.com/RubyMetric/chsrc.git -b dev
```

关于分支的说明，可参考 [./03-CONTRIBUTING.md](./03-CONTRIBUTING.md)

<br>


## 编译运行

```bash
make          # 默认使用 cc 编译
make CC=clang # 使用 clang 编译
make CC=gcc   # 使用 gcc   编译
```

```bash
# 重新编译并启动 GDB 调试
$ make debug

# 重新编译并启动 LLDB 调试
$ make debug DEBUGGER=lldb

# 如果需要单独生成含有编译信息的二进制文件（这个不会自己启动debugger）
$ make DEBUG=1
```

<br>

## 测试

```bash
make test-xy  # 测试 xy.h
make test-fw  # 测试 framework
make test     # 测试上述两个
make test-cli # 测试命令
make clean
```

<br>

## 提交 PR

关于分支的说明以及如何提交代码，请参考 [./03-CONTRIBUTING.md](./03-CONTRIBUTING.md)

<br>

[just]: https://github.com/casey/just
