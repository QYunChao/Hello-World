# Pro Git 简介

### 开始学习前先说一下关于 Git 的说明。

首先呢，我对 Git 本身算是有一定了解的，GitHub 我也经常逛，无论是对我个人的提升、还是对我工作的帮助，它所带来的都是难以估量的。但是我总觉得 GitHub 这个世界上最大的开源平台值其所代表的水平和所蕴含的价值，不应该如此浮于表面的，它值得、我也应当去更深入地去了解和学习它，它是一个平台，但是，不仅仅是一个平台。

好了，纲领性的一些东西说完了，落回实处，之所以选择`【Pro Git 第二版 简体中文】`这边书作为我系统学习Git第一本教材呢，是因为这本书也算是Git官方推荐的一本书吧，然后我自己大概浏览了下目录结构，觉得可行，所以就是它了。

### OK，学习正式开始——

Git 的官方地址：[GIT](https://git-scm.com/)

Pro Git 是 Git 官方推荐的学习书籍，书籍地址：[Pro Git 第二版 简体中文](http://git-scm.com/book/zh/v2)

如果下载不下来，可以试下 GitBook 上的另一个移植版本，感觉排版比官方版还好一点：[GitBook-progit2](https://legacy.gitbook.com/book/bingohuang/progit2/details)

>在这里，所记录的都会是我自己在随书学习过程中的一些心得，但过程中不可避免地会对原著做一些摘抄和引用，为了表示对原书的尊重和谢意，也为了让这里看起来内容更充实一些，将原书的序言和前言摘录如下。



**英文版**

## Preface by Scott Chacon

Welcome to the second edition of Pro Git. The first edition was published over four years ago now. Since then a lot has changed and yet many important things have not. While most of the core commands and concepts are still valid today as the Git core team is pretty fantastic at keeping things backward compatible, there have been some significant additions and changes in the community surrounding Git. The second edition of this book is meant to address those changes and update the book so it can be more helpful to the new user.

When I wrote the first edition, Git was still a relatively difficult to use and barely adopted tool for the harder core hacker. It was starting to gain steam in certain communities, but had not reached anywhere near the ubiquity it has today. Since then, nearly every open source community has adopted it. Git has made incredible progress on Windows, in the explosion of graphical user interfaces to it for all platforms, in IDE support and in business use. The Pro Git of four years ago knows about none of that. One of the main aims of this new edition is to touch on all of those new frontiers in the Git community.

The Open Source community using Git has also exploded. When I originally sat down to write the book nearly five years ago (it took me a while to get the first version out), I had just started working at a very little known company developing a Git hosting website called GitHub. At the time of publishing there were maybe a few thousand people using the site and just four of us working on it.

As I write this introduction, GitHub is announcing our 10 millionth hosted project, with nearly 5 million registered developer accounts and over 230 employees. Love it or hate it, GitHub has heavily changed large swaths of the Open Source community in a way that was barely conceivable when I sat down to write the first edition.

I wrote a small section in the original version of Pro Git about GitHub as an example of hosted Git which I was never very comfortable with. I didn’t much like that I was writing what I felt was essentially a community resource and also talking about my company in it. While I still don’t love that conflict of interests, the importance of GitHub in the Git community is unavoidable. Instead of an example of Git hosting, I have decided to turn that part of the book into more deeply describing what GitHub is and how to effectively use it. If you are going to learn how to use Git then knowing how to use GitHub will help you take part in a huge community, which is valuable no matter which Git host you decide to use for your own code.The other large change in the time since the last publishing has been the development and rise of the HTTP protocol for Git network transactions. Most of the examples in the book have been changed to HTTP from SSH because it’s so much simpler.

It’s been amazing to watch Git grow over the past few years from a relatively obscure version control system to basically dominating commercial and open source version control. I’m happy that Pro Git has done so well and has also been able to be one of the few technical books on the market that is both quite successful and fully open source.

I hope you enjoy this updated edition of Pro Git.

## Preface by Ben Straub

The first edition of this book is what got me hooked on Git. This was my introduction to a style of making software that felt more natural than anything I had seen before. I had been a developer for several years by then, but this was the right turn that sent me down a much more interesting path than the one I was on.

Now, years later, I’m a contributor to a major Git implementation, I’ve worked for the largest Git hosting company, and I’ve traveled the world teaching people about Git. When Scott asked if I’d be interested in working on the second edition, I didn’t even have to think.

It’s been a great pleasure and privilege to work on this book. I hope it helps you as much as it did me.

## Dedications

To my wife, Becky, without whom this adventure never would have begun. — Ben

This edition is dedicated to my girls. To my wife Jessica who has supported me for all of these years and to my daughter Josephine, who will support me when I’m too old to know what’s going on. —Scott

---


**中文版**

## Scott Chacon 序

欢迎来到 Pro Git 第二版。 第一版出版到现在已经过去了四年。 到今天，Git 虽然出现了许多改变，但是还有很多重要的事情一如昨日。 因为 Git 核心团队对保持向后兼容性异常固执，所以直到今天大多数核心命令与概念依然有效，但是围绕 Git 的社区还是有一些重大的增加与改变。 本书的第二版就是为了更新书籍并讲解那些改动以使其对新用户更有帮助。

当我写第一版时，Git 对于超级黑客来说还是一个相对难用，只能勉强接受的工具。 它开始在特定的社区中快速发展，但是还没有达到像今天一样无处不在的地步。 自那时起，几乎每一个开源社区都采用了它。 Git 在Windows 上取得了难以置信的进步，包括所有平台的图形用户界面对它的支持、IDE 的支持，以及商业使用的爆炸式发展。 四年前的 Pro Git 对此一无所知。 新版本的主要目标之一就是涉及 Git 社区中那些所有新的前沿领域。

使用 Git 的开源社区也呈现出爆炸式的发展。 大概在五年前吧，我坐下来写这本书时（写完第一个版本花了我不少时间），我开始在一个知名度极小的开发 Git 托管网站的公司工作，这家公司就是 GitHub。 本书出版时大概有几千人在使用 GitHub 网站，而为其工作的只有我们四个人。 在我写这篇介绍时，GitHub 宣布我们托管了1000 万个项目、拥有大概 500 万注册开发者账户与大概 230 名员工。 爱它也好，恨它也罢，当我坐下来写第一版时，GitHub 以一种意想不到的方式猛烈地改变了一大批开源社区。

我在 Pro Git 的原始版本中写了一节我并不是很满意的内容，是作为和提供 Git 托管服务相关的例子的 GitHub。我在书里写的东西本质上都是和社区有关的，但是又不得不讨论到我的公司，这点我不喜欢。 同时我还不喜欢那个兴趣的冲突，GitHub 在 Git 社区中的重要性是无法避免的。 我已经决定将本书的那部分转变为深度介绍
GitHub 是什么以及如何高效地使用它，而不再是作为一个 Git 托管的例子。 如果你正学习如何使用 Git，那么了解如何使用 GitHub 将会帮助你加入到一个巨大的社区中。不论你决定为自己的代码使用哪一个 Git 托管服务，这都很有价值。 自从上次出版以来另一个重大变革是 Git 网络传输 HTTP 协议的开发与崛起。书中的大多数例子都已经从 SSH切换到 HTTP，因为它更简单。

在过去这几年看到 Git 从一个相对无名的版本管理系统成长为商业与开源版本管理的事实标准是令人吃惊的。我很高兴 Pro Git 做得很好并已经成为市场上几本既成功又完全开源的技术书籍之一。

我希望你能享受这个升级版的 Pro Git。

## Ben Straub 序

本书的第一版就是将我与 Git 结下不解之缘的原因。书中采用的是我引进的做软件的风格，这种风格比我之前看到的任何事情都要自然。那时我已经做了好几年开发者了，但是这本书将我指引到一条更加精彩的道路上。

几年之后的现在，我是 Git 的一个主要实现的贡献者，我在最大的 Git 托管公司工作，我已经环游世界教人们使用 Git。当 Scott 问我是否有兴趣在第二版上工作时，我甚至连想都没想就答应了。能在这本书上工作是一份巨大的快乐与荣耀。

我希望它能像帮助我一样帮助你。

## 献辞

致我的妻子，Becky，没有她的话这段冒险不会开始。—— Ben

谨以此书献给我的家人。 给这些年一直支持着我的妻子 Jessica 和女儿 Josephine， 还有那些在我风烛残年之时还能支持我的人。—— Scott
