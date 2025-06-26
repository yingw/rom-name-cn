# ROM Name CN

本项目旨在为 No-Intro, Redump 等 ROM 数据整理网站提供的 ROM dat 数据提供一个相对统一的中文译名。

## 翻译范围

大致范围：雅达利、FC 时代（198X）到 PS2/XBOX/3DS 时代（201X），一个原因是再早的平台我也不熟悉了，另一边是从 PS3 开始，大部分游戏平台都有了国行版，游戏都有了中文官方译名。

:white_check_mark: 已翻译的平台：

- 任天堂：
  - 家用机：FC（NES）, SFC（SNES）, N64, GameCube, Wii, Wii U, Virtual Boy, Famicom Disk System；
  - 掌机：Game & Watch, GameBoy, GameBoy Color, GameBoy Advance, NDS（90%）,3DS, Pokemon Mini
- 世嘉：MD, CD, 32X, GameGear, Saturn, DreamCast, Master System - III
- 索尼：PS1, PSP
- SNK：NeoGeo Pocket, NeoGeo Pocket Color
- 万代：神奇天鹅, 神奇天鹅 彩色版
- 街机：Mame（90%），还分了 CSP1～3/FBA 等
- NEC：PC-Engine, PC-Engine SuperGrafx
- 雅达利：2600, 5200, 7800, Lynx
- 松下 3DO

:hourglass: 待翻译平台：

- PS2, PSV, XBOX, Wii U
:x: 一些暂时无法翻译的平台（主要是数量太多或缺失dat）：

- MSX, PC/Dos, J2ME, ScummVM

## dat 数据来源

- [no-intro](https://datomatic.no-intro.org/) - 卡带类游戏 dat
- [ReDump](http://redump.org/) - 光碟类平台游戏 dat
- [Mame](https://www.mamedev.org/) - 街机模拟器，dat 数据使用一些工具从其中提取出，以及网站[progetto-SNAPS](https://www.progettosnaps.net/index.php)采集整理
- [英化版 dat](https://archive.org/download/En-ROMs/DATs/)  - 英化版 dat*
- [libretro-database](https://github.com/libretro/libretro-database) - 一些比较小众的平台采用 libretro 整理的 dat，只是许久不更新了

> \* 英化版即是国外一些“英化组”或个人，他们将一些没有英文版的日版游戏“英化”成英语版，类似国内的“汉化版”，比如“逆转裁判123”，这些游戏原本应该和 dat 一一对应，但是由于“英化组”采用的英文名很可能是旧版本 dat，或者自己做了翻译，比如“逆转裁判”的 dat 名称即为：`Gyakuten Saiban`，这其实是日语的英文发音写法，英化组会采用他们看得懂的`Phoenix Wright - Ace Attorney`，这也是逆转系列后续平台美版欧版的官方名称，为保持一致，将这部分数据也纳入进来并做了和中文对照

## 翻译格式说明

目前仅提供了 CSV 文件格式数据（未来如果有多字段需求考虑改成 json），输出有2个版本：

1. 仅翻译`游戏名称`，即：`Ace of Aces (USA)` 翻译为：`王牌飞行员`，即只翻译了游戏名称部分，游戏的后缀（也叫：代码，英文：Code、Decoration）并不翻译。（后面会提到会在另一个项目里统一翻译）
2. 翻译`名称+代码`，即：`Ace of Aces (USA)` 翻译为：`王牌飞行员(美版)`。这个记录方法的好处是完整，确定是格式一旦定了，改了就麻烦，后续用另一个项目可以进行自动翻译和自定义格式。这里提供了一个默认的代码翻译结果。参考[代码说明](#代码说明)

目前可能个别平台的翻译结果文件 `*.csv` 采用的还是方式2，逐步更新。

关于名称的取舍

有时候，一个游戏会有多个历史不同版本、或者不同团队的翻译方式，这里基本上采用了：

- 大 IP 统一：如 马里奥、索尼克 等等，这里收集整理了 50 多个大 IP 的常见译名和采用的译名，参考[别名](#别名)，如果有定制需求，可以参考：可以在设置了希望使用的译名后动态产生不同的翻译结果
- 百度指数 - 一个游戏的多个译名如果存在多个，而且并没有哪个特别不合理的情况下，采用百度指数对比，有些不大的 IP 就不记录在上述的多译名选择中了。
- AI 翻译和建议：是的，即使在翻译过程中，我也采用了：名称 + 简介 + 定制需求 的方式来让多个 AI 帮我翻译和取舍，简单说就是将游戏的原英文名和从 ss 刮削来的简介发给 AI，并附上特点的要求（如字数、风格）来让 AI 翻译并互相评判

关于名称的格式

中文翻译用在文件名上，还有特殊字符

乱马1/2 文件名不能有“/”

## 已翻译的记录

家用机：

| 平台                                                                              | 版本                 | ROM 数    | 完成度                           |
| --------------------------------------------------------------------------------- | -------------------- | --------- | -------------------------------- |
| [任天堂 FC/NES](./Nintendo%20-%20Nintendo%20Entertainment%20System.csv)           | 20250317 (Retail)    | 2428      | ![Completed 100%][Completed 100] |
| [任天堂 SFC/SNES](./Nintendo%20-%20Super%20Nintendo%20Entertainment%20System.csv) | 20250318 (Retail+ST) | 3139      | ![Completed 100%][Completed 100] |
| [任天堂 N64](./Nintendo%20-%20Nintendo%2064.csv)                                  | 20250208             | 1137      | ![Completed 100%][Completed 100] |
| 任天堂 FDS                                                                        | 待更新               | 324       |                                  |
| [任天堂 NGC](./Nintendo%20-%20GameCube.csv)                                       | 20250601 (Retail)    | 1785/2011 | ![Completed 100%][Completed 100] |
| [任天堂 Wii](./Nintendo%20-Wii.csv)                                               | 2025-05-17           | 3412/3776 | ![Completed 100%][Completed 100] |
| 任天堂 Wii/WiiU                                                                   |                      | 3772      | ![Not Started][Not Started]      |
| [索尼 PS1](./Sony%20-%20PlayStation.csv)                                          | 20250329 (Retail)    | 6193      | ![Completed 100%][Completed 100] |
| [世嘉 MD/Gensis](./Sega%20-%20Mega%20Drive%20-%20Genesis.csv)                     | 20250305 (Retail)    | 1591      | ![Completed 100%][Completed 100] |
| [世嘉 SS](./Sega%20-%20Saturn.csv)                                                | 待更新               | 1956      | ![Completed 100%][Completed 100] |
| [世嘉 DC](./Sega%20-%20Dreamcast.csv)                                             | 待更新               | 1124      | ![Completed 100%][Completed 100] |
| [世嘉 CD](./Sega%20-%20Mega%20CD%20&%20Sega%20CD.csv)                             | 2025-01-21           | 543       | ![Completed 100%][Completed 100] |
| 微软 MSX1                                                                         |                      | 0/936     | ![In Progress][In Progress]      |
| [微软 MSX2](./Microsoft%20-%20MSX2.csv)                                           |                      | 195       |                                  |
| [雅达利 2600](./Atari%20-%20Atari%202600.csv)                                     | 20250501             | 845       | ![Completed 100%][Completed 100] |
| [雅达利 5200](./Atari%20-%20Atari%205200.csv)                                     | 20250406             | 182       | ![Completed 100%][Completed 100] |
| [雅达利 7800](./Atari%20-%20Atari%207800.csv)                                     | 20250416             | 126       | ![Completed 100%][Completed 100] |
| [NEC PC Engine (TurboGrafx-16)](./NEC%20-%20PC%20Engine%20-%20TurboGrafx-16.csv)  | 20250224             | 454       | ![Completed 100%][Completed 100] |
| [NEC PC Engine SuperGrafx](./NEC%20-%20PC%20Engine%20SuperGrafx.csv)              | 20250121             | 5         | ![Completed 100%][Completed 100] |

<!-- 
[任天堂 FDC](./Nintendo%20-%20Family%20Computer%20Disk%20System.csv) | 315/323 | ![Completed 98%](https://img.shields.io/badge/Completed-98%25-green)
索尼 PS2* | 0/10835 | ![Not Started][Not Started]
世嘉 SEGA32x* | 0/206 | ![In Progress][In Progress]
世嘉 SEGA CD* | | ![Not Started][Not Started]
SNK NEO CD | | ![Not Started][Not Started]
PICO-8、ONS、PortMaster
[Completed 100%][Completed 100]
松下 3DO | | ![Not Started][Not Started]
 -->

掌机：

| 平台                                                                | 版本              | ROM 数    | 完成度                             |
| ------------------------------------------------------------------- | ----------------- | --------- | ---------------------------------- |
| [任天堂 GB](./Nintendo%20-%20Game%20Boy.csv)                        | 20250316 (Retail) | 1574      | ![Completed 100%][Completed 100]   |
| [任天堂 GBC](./Nintendo%20-%20Game%20Boy%20Color.csv)               | 20250314 (Retail) | 1393      | ![Completed 100%][Completed 100]   |
| [任天堂 GBA](./Nintendo%20-%20Game%20Boy%20Advance.csv)             | 20250313 (Retail) | 3046      | ![Completed 100%][Completed 100]   |
| [任天堂 NDS](./Nintendo%20-%20Nintendo%20DS.csv)                    | 20250304 (Retail) | 6996/7092 | ![In Progress 97%][In Progress 90] |
| [任天堂 3DS](./Nintendo%20-%20Nintendo%203DS.csv)                   | 20250502 (Retail) | 1870      | ![Completed 100%][Completed 100]   |
| [任天堂 New 3DS](./Nintendo%20-%20New%20Nintendo%203DS.csv)         | 20250110          | 11/11     | ![Completed 100%][Completed 100]   |
| [任天堂 Game &amp; Watch](./Nintendo%20-%20Game%20%20&%20Watch.csv) | 20241105          | 53        | ![Completed 100%][Completed 100]   |
| [任天堂 宝可梦迷你](./Nintendo%20-%20Pokemon%20Mini.csv)            | 20250407          | 44        | ![Completed 100%][Completed 100]   |
| [索尼 PSP](./Sony%20-%20PlayStation%20Portable.csv)                 | 20250329          | 3131      | ![Completed 100%][Completed 100]   |
| [世嘉 GG](./Sega%20-%20Game%20Gear.csv)                             | 20241203          | 818       | ![Completed 100%][Completed 100]   |
| [万代 WS](./Bandai%20-%20WonderSwan.csv)                            | 20241208 (Retail) | 125       | ![Completed 100%][Completed 100]   |
| [万代 WSC](./Bandai%20-%20WonderSwan%20Color.csv)                   | 20250117 (Retail) | 108       | ![Completed 100%][Completed 100]   |
| [SNK NGP](./SNK%20-%20Neo%20Geo%20Pocket.csv)                       | 20250222          | 10        | ![Completed 100%][Completed 100]   |
| [SNK NGPC](./SNK%20-%20Neo%20Geo%20Pocket%20Color.csv)              | 20240506          | 127       | ![Completed 100%][Completed 100]   |

<!-- 
NDSi的可能要实机测试
任天堂 NDSi | 0/1069 | ![In Progress][In Progress]
任天堂 3DS eShop | 0/975 | ![In Progress][In Progress]
任天堂 Game & Watch | 21/59 | ![In Progress 35%](https://img.shields.io/badge/In%20Progress-35%25-yellowgreen)
索尼 PSP(PSN) | 0/2019 | ![In Progress][In Progress]
-->

街机：

| 平台                                    | ROM 数  | 完成度                           |
| --------------------------------------- | ------- | -------------------------------- |
| MAME                                    |         | ![Not Started][Not Started]      |
| [CAPCOM CPS1](./Arcade%20-%20CPS1.csv)  | 185/185 | ![Completed 100%][Completed 100] |
| [CAPCOM CPS2](./Arcade%20-%20CPS2.csv)  | 299/299 | ![Completed 100%][Completed 100] |
| [CAPCOM CPS3](./Arcade%20-%20CPS3.csv)  | 37/37   | ![Completed 100%][Completed 100] |
| [SNK NeoGeo](./Arcade%20-%20NEOGEO.csv) | 257/257 | ![Completed 100%][Completed 100] |
| 世嘉 Naomi                              |         | ![In Progress][In Progress]      |
| 世嘉Sammy Atomiswave                    |         | ![In Progress][In Progress]      |

关于 Retail 过滤的说明：

原则上，每个平台的 dat 也并非 No-Intro 和 Redump 发布的 dat 全部内容，而是先用工具过滤一遍：Retail。因为这些 dat 里面大多包含了一些官方平台未正式发布的 ROM dat，如尚在开发过程中发布出来的 beta 版，后续取消开发、一些平台生命周期结束后第三方平台发布制作的一些游戏、一些官方/非官方组织的线下活动或比赛的奖品、一些定制版的游戏ROM，这些被 No-Intro 和 Redump 打上了特殊标记的

Dat 数据源过滤规则（一般）：
No-Intro：Exclude: x### ROMs/Proto/Beta/Demo/Aftermarket/Pirate/Unlicensed/BIOS...

但是也有例外

- 如有些平台游戏本来也不多，这些特殊 ROM 也一般都被放在 set 里
- 一些平台，即使在平台生命周期中，由于多种原因，中一些非英语、日语地区，一些企业开发的“非官方”游戏，如 MD 时代的很多台湾厂商开发的中文游戏
- 一些平台即使生命周期很后面，也有不少企业或开发者还在为这个平台开发的一些比较知名的游戏，如 2023 年正式发布的《好狗狗星系》

这些也尽量收录进翻译中。

各平台使用的数据源：

- 世嘉 MD/Gensis - `Sega - Mega Drive - Genesis (20240907-224108).dat` 除去 Demo 等：1714；Retool 除去 15 个 promram、1 个 HeartBeat Catalyst，最终：1698
- 世嘉 GameGear - `Sega - Game Gear (20240827-211557)` 812；除去 Demo 等后：469
- 任天堂 GBA - `Nintendo - Game Boy Advance (#3120 + x462).dat` 3562；除去 xXXX、Demo 后：2850
- 任天堂 FC/NES - `Nintendo - Nintendo Entertainment System (Headerless) (20240829-004657).dat` 4170，去除各种后 2247
- 任天堂 SFC/SNES - `Nintendo - Super Nintendo Entertainment System (20240830-122750).dat` 去掉各种 Demo 后，3145（更新：3070）
- 任天堂 N64 - `Nintendo - Nintendo 64 (BigEndian) (20240908-020954).dat` 去掉各种 Demo、Beta 等：962；再用 Retool 去掉 (Wii Virtual Console)，(GameCube)，(LodgeNet) ，(Switch Online)、Wide-Boy64，最后：896 个
- 世嘉 Saturn（土星） - ReDump 数据：`Sega - Saturn - Datfile (2370) (2024-09-17 15-43-36).dat`，2370，去掉各种程序、Demo，各种乱数据，最后 1956
- 世嘉 Dreamcast(DC) - ReDump 数据： `Sega - Dreamcast - Datfile (1488) (2024-09-13 14-42-29).dat`，1488，去掉各种程序、Demo，最终：1224
- PS1 目前还没头绪，10000多个游戏，去重后还有 6000 多，再去掉非美区、日区（因为一样的游戏不一样名称），巴哈有 2000 多翻译
- 任天堂 GB - `Nintendo - Game Boy (20240914-013134).dat` 1931，处理后 1621，删掉了 (Limited Run Games)、(Retro Collection)、(QUByte Classics) 三个在线平台
- 任天堂 GBC - `Nintendo - Game Boy Color (20240919-003154).dat` 1946，去除各种后 1394
- 任天堂 3DS - `Nintendo - Nintendo 3DS (Decrypted) (#1870 + x062 + z207).dat` 去掉 x### 和 z### 后 1870

整理用到的一部分工具

- RomCenter
- Retool
- CLRMamePro

测试平台

- RetroArch
- EmuELEC
- ES-DS
- ArkOS
- OnionUI

基本上在 EmulationStation 前端的模拟平台上能正常显示中英文

本项目的基础翻译来源于几个较大的模拟器论坛玩家整理的中英文对照表，主要有：

- [老男人游戏网](https://www.oldmanemu.net/) - 国内最大的模拟资源基地。站长多年坚持运维和更新各系统游戏列表，有不少是已经整理了和No-Intro对照的中英文了。
- [Emumax](http://www.emumax.com/roms) - 打不开了，去年还可以的
- [维基百科：各平台游戏列表](https://zh.wikipedia.org/wiki/Category:%E5%90%84%E5%B9%B3%E5%8F%B0%E9%81%8A%E6%88%B2%E5%88%97%E8%A1%A8) - 这个列表的中英日文列表里面，又一部分是有中文翻译的，而且游戏还有链接，用来考证翻译正确性很有用。
- [A9VG 论坛](https://bbs.a9vg.com/) - 老牌游戏论坛
- [琵琶行论坛](https://www.ppxclub.com/) - 琵琶行论坛上之前有很多整理得不错的列表，但是很可惜，这两年一直各种问题，今年彻底上不去了。这也是我今年想起来把这个项目补充完整的重要原因之一。
- [豆瓣](https://www.douban.com/game/explore) - 豆瓣的游戏板块其实有很多外面找不到的老游戏的中英日文名称和介绍，而且翻译质量高，缺点是要一个个找，如 SFC 的
- [篝火营地](https://gouhuo.qq.com/games/library) - 仓库内容也不少，和豆瓣差不多，缺点是只有中文，得看图识字。
- [浮游城](http://bbs.chinaemu.org/read-htm-tid-18465.html) - 浮游城的版主 Lobelia 在 05 年整理的十几个列表
- [巴哈姆特 j9y6638的小屋](https://home.gamer.com.tw/creationCategory.php?owner=j9y6638&c=435712) - 巴哈博主 夏凰翔 整理的超多列表，但是格式有点乱
- [精英模拟网](http://emu.jy6d.com/dz/) - 专门有个中英文对照表的板块，整理了十六个平台的中英文对照表，看数据应该也是比较老的，格式也有点乱
- [INDIENOVA](https://ld0.indienova.com/gamedb/platform/saturn/p/1) - 很不错的游戏库，游戏配了中英文名称，有些也比较小众外面没见过，缺点是首页的列表只做了几个新的游戏平台，得搜索。
- [小鸡模拟器](https://wwww.xiaoji001.com/xiaoji.php?s=index-gamelist-type-NDS) - 小鸡作为模拟平台，游戏比较全，中文翻译也比较彻底，缺点是没有英文
- [i3DS.fun](https://i3ds.fun/) - 3DS的专题网站，3DS的翻译最全，最近也在维护
- [掌机迷](https://www.gbarom.cn/pspyxml) - 可以看出站长也在整理类似的对照表，可下载几个平台目录的Excel文档
- [GameTDB](https://www.gametdb.com/) - GameCube 和 Wii 的中文名称翻译来源
- 其他还许多随机找的不一一列举，一并感谢

英文数据主要来源：

- [Reddit](https://www.reddit.com/r/Roms/)
- [Mame](https://github.com/retropie/retropie-setup/wiki/MAME)
- [ピコピコ大百科](https://www.gavas.jp/) - 查日语游戏名
- [Screen Scraper](https://www.screenscraper.fr/) - 查游戏图片、视频
- [mobygames](https://www.mobygames.com/platform/) - 游戏图、介绍，有收费API

[In Progress]: https://img.shields.io/badge/In%20Progress-0%25-yellow
[In Progress 90]: https://img.shields.io/badge/In%20Progress-90%25-yellow
[Not Started]: https://img.shields.io/badge/Not%20Started-0%25-red
[Completed 100]: https://img.shields.io/badge/Completed-100%25-brightgreen

## 代码说明

## 别名

目前整理了 69 个大游戏 IP 极其常见的别名，见  [别名](./alias.md)，格式如下：

```json
    "Tactics Ogre": {
        "alias-en": [
            "Ogre Battle"
        ],
        "alias": [
            "皇家骑士团",
            "奥迦战争"
        ],
        "default": "皇家骑士团",
        "others": [
            "奥伽战争",
            "奥加战争"
        ]
    },
```

json Key 为英文名，alias-en 为可能得英文别名（可选），alias 为整理到的中文别名，default 为默认的中文翻译用名称，others 为其他见到的但未支持的中文别名。

此外还有一种特殊的 exclude ：

```json

    "Sonic": {
        "alias": [
            "索尼克",
            "音速小子"
        ],
        "default": "索尼克",
        "exclude": [
            "Sonic Blast Man",
            "Sonic Wings"
        ]
    },
```

表示正好有其他游戏的英文名中也包含了这里的 Sonic，但是不依据这个 IP 的翻译。

这个 json 文件放在这里仅供参考使用，具体的用法参考项目<>。

## 协作

本项目的翻译内容大部分来源于网上和我个人的翻译，如果你有更好的翻译参考，或者有兴趣帮忙翻译一些还未完成的平台，亲参考：[贡献](./CONTRIBUTING.md)。
