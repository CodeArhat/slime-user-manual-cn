一、简介
========

SLIME 即“Emacs的高级交互式Lisp开发模式”。

SLIME扩展了Emacs以支持Common Lisp交互式编程。作为Emacs标准lisp-mode的扩充，其特性集中在slime-mode中。虽然lisp-mode也支持编辑Lisp源码，但slime-mode还能与运行中的Common Lisp进程交互，进行编译、调试、查找文档等工作。

slime-mode开发环境效仿Emacs原生的Emacs Lisp环境。我们吸取了类似系统（例如ILISP）的优点，也加入了一些我们自己的想法。

SLIME由两部分组成：用户界面（用Emacs Lisp编写），服务程序（用Common Lisp编写）。双方通过socket互联，并用一种类似RPC的协议通信。

服务端主要用可移植的Commom Lisp写成。与具体Lisp实现相关的必要功能定义成一个精心设计的接口，并为各种Lisp分别实现。这使得SLIME非常容易移植。
