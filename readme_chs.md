﻿# BlokusHacker

> 角斗士棋的AI

***不断更新中……***

[角斗士棋](http://www.mattelgames.com/en-us/blokus/index.html) 是[Bernard Tavitian](https://en.wikipedia.org/wiki/Blokus#cite_note-2)发明的一种供2至4人游戏的抽象策略类桌游。最早于2000年由法国企业Sekkoïa发行。角斗士棋曾获得过包括国际游戏节门萨奖及2004年度教师选择奖等很多奖。
![Blokus](BLOKUS.jpg)
*图片取自 http://www.mattelgames.com*

角斗士棋AI比赛是为中国科大学生举办的比赛，我们衷心祝愿每个参赛选手设计出多种多样的AI程序。
主办方将会为各个选手的AI提供相互PK的平台。

## 规则

角斗士棋的棋盘分为20行20列总共400小格。4个玩家分别执红黄绿蓝四色棋子，每位玩家的棋子有21种。每个棋子由1到5个方块组成（包括1个单方块的，1个双方块的，2个三方块的，5个四方块的和12个五方块的）

![Tiles](Tiles.png)

角斗士棋各种玩法的标准规则如下：

* 落子的顺序既可以是顺时针也可以逆时针
* 每位玩家的第一颗子必须下在棋盘的四角。玩家落子时，同颜色棋子的方块只能角对角相连，不能边对边。但当两种颜色的棋子交错时，可以与同种颜色棋子的边相连落子
* 当某一个玩家无棋可下时，直接跳过该玩家，游戏正常进行。当所有玩家都无棋可下时，游戏结束
* 游戏结束后，每位玩家所下棋子的方块数即为该玩家的得分（比如某玩家下了一枚四方块的棋子，那么就可以获得4分）。如果某位玩家把他所有的子都下完了，那么他可以获得15分额外的奖励，并且如果他最后下的棋子是一方块的，可以再获5分奖励


## 限制

为了公平起见，比赛采取2对2的方式进行，并且棋盘大小为14*14，两位玩家各执一色，第一步需要包含一个特殊位置。


因为暴力搜索的复杂度大约在1074~10100，所以你需要寻找一些更加高端的方式。

![SmallBoard](SmallBoard.png)

**棋盘上的坐标规定：**

![GridIndexing](GridIndexing.png)


**以下是优胜者的标准（可选）：**

* 在给定充足思考的时间下获取最高分（比如每步30秒）
* 在非常有限的思考时间下获取最高分（比如每步1秒）
* 不预先训练，不预先搜索
* 可拓展性（暴力搜索不满足可拓展性）
* 找到AI的某些漏洞
* *其他标准正在增加，敬请期待*

达到以上标准一项或几项的都是十分光荣的

##示例程序
###Blokus-0405.py
>更多细节请访问BlokusHacker/Example/site .

示例程序可以让你迅速的写出你自己的角斗士棋AI，代表AI水平的核心的功能是getScores。
如果你不想浪费时间在一些像rotate, canPut, getDiagList之类的基础功能上，我们欢迎你使用示例程序中的代码。
**:)**.
