# 前言 Preface

=======

老子说过:道生一,一生二,二生三,三生万物.

像极了~~爱情~~编程

Programmers shape ideas into text.
程序猿把创意,灵感,逻辑整理进文本

That text gets turned into numbers and those numbers bump into other numbers
and *make things happen*.
这些文本被机器翻译成以高低电平代表的数码，这些010101的数字流通过传输与其他数字流彼此交融碰撞.
*带来了魔幻的自动化*.

As programmers, we use text editors to get our ideas out of our heads and create
the chunks of text we call "programs".  Full-time programmers will spend tens of
thousands of hours of their lives interacting with their text editor, during
which they'll be doing many things:
作为程序员，我们使用文本编辑器把我们的想法一一具现，具现留下来的产物是被我们称之为“程序”的文本块。
职业程序员将在职业生涯中花费数万小时(主要来自加班)与他们的文本编辑器进行深入♂交流，交流内容如下:

* Getting raw text from their brains into their computers.
把他们脑海里不敢让语文老师看见的文本藏进电脑
* Correcting mistakes in that text.
把文本里为数不多的正确部分挑出来
* Restructuring the text to formulate a problem in a different way.
把挑剩下的搞不定的问题一一转换成搞得定的问题——实在搞不定的问题会被转换成BUG。
* Documenting how and why something was done a particular way.
写注释,记录一下这些bug是怎么解决的,用了哪种姿势进行的Ctrl-C+V.
不写注释的话连写代码的人自己都看不懂自己写的是个啥.
没解决的烂摊子也用注释标记一下,好让后来者痛哭流涕，感受正道的光.
* Communicating with other programmers about all of these things.
上大型同性交友平台和其他~~CtrlCVer~~程序员打招呼:今天你bug了吗

Vim is incredibly powerful out of the box, but it doesn't truly shine until you
take some time to customize it for your particular work, habits, and fingers.
This book will introduce you to Vimscript, the main programming language used to
customize Vim.  You'll be able to mold Vim into an editor suited to your own
personal text editing needs and make the rest of your time in Vim more
efficient.
Vim 就是一个非常强大的文本编辑器，但是如果你不花点时间为你的工作、习惯和手指定制 Vim，它就不会真正出彩。
本书将向您介绍 Vimscript —— 一种主要用于自定义 Vim 的编程语言。你可以个性化定制 Vim  
把它打造成一个适合自己个人文本编辑需要的编辑器，并且使你日后 在 Vim 中的花费的时间更有效率。

Along the way I'll also mention things that aren't strictly about Vimscript, but
are more about learning and being more efficient in general.  Vimscript isn't
going to help you much if you wind up fiddling with your editor all day instead
of working, so it's important to strike a balance.
在这个过程中，我还会提到一些不是严格意义上的 Vimscript，而是关于学习和提高效率的东西。
如果你整天都在和你的编辑器玩耍而不是工作，目前来说 Vimscript 对你的提升没有多大帮助，
所以找到一个平衡点很重要。

The style of this book is a bit different from most other books about
programming languages.  Instead of simply presenting you with facts about how
Vimscript works, it guides you through typing in commands to see what they do.
这本书的风格有点不同于其他大多数关于编程语言的书。
它不是简单地向你展示 Vimscript 是如何工作的，把结论直接抛给你。
而是抛出问题与练习引导你输入命令，实际动手敲打键盘做实验，来检验它们是如何工作的。

Sometimes the book will lead you into dead ends before explaining the "right
way" to solve a problem.  Most other books don't do this, or only mention the
sticky issues *after* showing you the solution.  This isn't how things typically
happen in the real world, though.  Often you'll be writing a quick piece of
Vimscript and run into a quirk of the language that you'll need to figure out.
By stepping through this process in the book instead of glossing over it I hope
to get you used to dealing with Vimscript's peculiarities so you're ready when
you find edge cases of your own.  Practice makes perfect.
有时候，在解释解决问题的“正确方法”之前，这本书会把你引入死胡同。
大多数书籍都不会这样做，或者会在向你展示解决方案之后才提到棘手的问题。
然而，在现实世界中，事情通常不是这样发生的，优秀的程序员往往是在充满挑战的境地下，
一次接一次地探索着更好的解决方案。通常情况下，你在写一篇关于 Vimscript 的文章时，会遇到一些你需要搞清楚的语言问题。
通过在书中逐步介绍这个过程，而不是对这一磕磕绊绊的过程进行修饰，
我希望能让你习惯于处理 Vimscript 的特性，这样当你发现自己碰到了没人接触过的案例时，你就已经准备好了。
熟能生巧。

Each chapter of the book focuses on a single topic.  They're short but packed
with information, so don't just skim them.  If you really want to get the most
out of this book you need to actually type in all of the commands.  You may
already be an experienced programmer who's used to reading code and
understanding it straight away.  If so: it doesn't matter.  Learning Vim and
Vimscript is a different experience from learning a normal programming language.
这本书的每一章都集中在一个单一的主题上。它们很短，但是却包含了大量的信息，所以不要只是浏览。
如果你真的想充分利用这本书，你需要输入所有的命令。你可能已经是一个经验丰富的程序员，习惯了直接阅读代码并理解它。
如果是这样的话，那没关系。学习 Vim 和 Vimscript 与学习普通编程语言是不同的经历。

* You need to **type in *all* the commands.**
**在键盘上敲入*所有*的命令。**

* You need to **do *all* the exercises.**
**动脑思考演算*所有*的问题。**

There are two reasons this is so important.  First, Vimscript is old and has
a lot of dusty corners and twisty hallways.  One configuration option can change
how the entire language works.  By typing *every* command in *every* lesson and
doing *every* exercise you'll discover problems with your Vim build or
configuration on the simpler commands, where they'll be easier to diagnose and
fix.
这一点如此重要有两个原因。首先，Vimscript 已经发展了很久，有很多积满历史灰尘的角落和记载他前进过程的弯区走廊。
一个配置选项可以改变整个语言的工作方式。通过在每个课程中输入*所有*命令并做*所有*练习，
你将发现你的 Vim 构建或配置在更简单的命令上的问题，这些命令将更容易诊断和修复。

Second, Vimscript *is* Vim.  To save a file in Vim, you type `:write` (or `:w`
for short) and press return.  To save a file in a Vimscript, you use `write`.
Many of the Vimscript commands you'll learn can be used in your day-to-day
editing as well, but they're only helpful if they're in your muscle memory,
which simply doesn't happen from just reading.
其次，Vimscript 是 Vim 的一部分。想要在 Vim 中保存文件，需要输入`: write` (或缩写成`: w`) ，然后按 return。
要在 Vimscript 中保存文件，可以使用`write`。你将学到的许多 Vimscript 命令也可以用于你的日常编辑，
但是只有它们被你的手指所记忆时才能发挥效果，而想凭借阅读达成肌肉记忆是相当困难的。

I hope you'll find this book useful.  It's *not* meant to be a comprehensive
guide to Vimscript.  It's meant to get you comfortable enough with the language
to mold Vim to your taste, write some simple plugins for other users, read other
people's code (with regular side-trips to `:help`), and recognize some of the
common pitfalls.
我希望你会觉得这本书有用。这本书并不打算成为一本 Vimscript 的全面指南。
它的目的是让你对这门语言足够熟悉，以便按照自己的口味塑造 Vim，为其他用户编写一些简单的插件，
阅读其他人的代码(通过定期的`:help`之旅) ，并识别一些常见的陷阱。

Good luck!
