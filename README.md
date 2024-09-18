# ROM Name CN

![In Progress](https://img.shields.io/badge/In%20Progress-16-yellow)
![Completed](https://img.shields.io/badge/Completed-13-brightgreen)
![Not Started](https://img.shields.io/badge/Not%20Started-9-red)

基于 [no-intro](https://datomatic.no-intro.org/) 的英文版 ROM 名称的中英文对照。也希望大家一起[贡献](./CONTRIBUTING.md)。

家用机：

平台 | ROM 数 | 完成度
---|---|---
[任天堂 FC/NES](./Nintendo%20-%20Nintendo%20Entertainment%20System.csv) | 2247/2247 | ![Completed 100%][Completed 100]
任天堂 SFC/SNES | 0/3625 | ![In Progress][In Progress]
[任天堂 FDC](./Nintendo%20-%20Family%20Computer%20Disk%20System.csv) | 315/323 | ![Completed 98%](https://img.shields.io/badge/Completed-98%25-green)
[任天堂 N64](./Nintendo%20-%20Nintendo%2064.csv) | 896/896 | ![Completed 100%][Completed 100]
索尼 PS1 | 0/10066 | ![Not Started][Not Started]
索尼 PS2 | 0/10835 | ![Not Started][Not Started]
[世嘉 MD/Gensis](./Sega%20-%20Mega%20Drive%20-%20Genesis.csv) | 1698/1698 | ![Completed 100%][Completed 100]
世嘉 SS | | ![Not Started][Not Started]
世嘉 DC | | ![Not Started][Not Started]
世嘉 SEGA32x | 0/206 | ![In Progress][In Progress]
世嘉 SEGA CD* | | ![Not Started][Not Started]
微软 MSX1 | 0/936 | ![In Progress][In Progress]
[微软 MSX2](./Microsoft%20-%20MSX2.csv) | 195/195 | ![Completed 100%][Completed 100]
SNK NEO CD | | ![Not Started][Not Started]
松下 3DO | | ![Not Started][Not Started]

掌机：

平台 | ROM 数 | 完成度
---|---|---
任天堂 GB | 0/1645 | ![In Progress][In Progress]
任天堂 GBC | 0/1471 | ![In Progress][In Progress]
[任天堂 GBA](./Nintendo%20-%20Game%20Boy%20Advance.csv) | 2850/2850 | ![Completed 100%][Completed 100]
任天堂 Game & Watch | 21/59 | ![In Progress 35%](https://img.shields.io/badge/In%20Progress-35%25-yellowgreen)
[任天堂 NDS](./Nintendo%20-%20Nintendo%20DS.csv) | 6172/7180 | ![Completed 86%](https://img.shields.io/badge/Completed-86%25-green)
任天堂 NDSi | 0/1069 | ![In Progress][In Progress]
任天堂 3DS | 0/1942 | ![In Progress][In Progress]
任天堂 3DS eShop | 0/975 | ![In Progress][In Progress]
任天堂 New 3DS | 0/10 | ![In Progress][In Progress]
索尼 PSP | 0/3451 | ![In Progress][In Progress]
索尼 PSP(PSN) | 0/2019 | ![In Progress][In Progress]
[世嘉 GG](./Sega%20-%20Game%20Gear.csv) | 469/469 | ![Completed 100%][Completed 100]
[万代 WS](./Bandai%20-%20WonderSwan.csv) | 125/125 | ![Completed 100%][Completed 100]
[万代 WSC](./Bandai%20-%20WonderSwan%20Color.csv) | 100/100 | ![Completed 100%][Completed 100]
[SNK NGP](./SNK%20-%20Neo%20Geo%20Pocket.csv) | 10/10 | ![Completed 100%][Completed 100]
[SNK NGPC](./SNK%20-%20Neo%20Geo%20Pocket%20Color.csv) | 116/116 | ![Completed 100%][Completed 100]

街机：

平台 | ROM 数 | 完成度
---|---|---
MAME | | ![Not Started][Not Started]
[CAPCOM CPS1](./Arcade%20-%20CPS1.csv) | 185/185 | ![Completed 100%][Completed 100]
[CAPCOM CPS2](./Arcade%20-%20CPS2.csv) | 299/299 | ![Completed 100%][Completed 100]
[CAPCOM CPS3](./Arcade%20-%20CPS3.csv) | 37/37 | ![Completed 100%][Completed 100]
[SNK NeoGeo](./Arcade%20-%20NEOGEO.csv) | 257/257 | ![Completed 100%][Completed 100]
世嘉 Naomi | | ![In Progress][In Progress]
世嘉Sammy Atomiswave | | ![In Progress][In Progress]

Dat 数据源过滤规则（一般）：
No-Intro：Exclude: x### ROMs/Proto/Beta/Demo/Aftermarket/Pirate/Unlicensed/BIOS...

英文数据主要来源：

- [no-intro](https://datomatic.no-intro.org/)
- [Reddit](https://www.reddit.com/r/Roms/)
- [Mame](https://github.com/retropie/retropie-setup/wiki/MAME)
- [libretro-database](https://github.com/libretro/libretro-database)

中文数据主要来源：

- [老男人游戏网](https://www.oldmanemu.net/)
- [Emumax](http://www.emumax.com/roms)
- [维基百科](https://zh.wikipedia.org/wiki/%E7%94%B5%E5%AD%90%E6%B8%B8%E6%88%8F)
- [A9VG 论坛](https://bbs.a9vg.com/)
- [琵琶行论坛](https://www.ppxclub.com/)

[In Progress]: https://img.shields.io/badge/In%20Progress-0%25-yellow
[Not Started]: https://img.shields.io/badge/Not%20Started-0%25-red
[Completed 100]: https://img.shields.io/badge/Completed-100%25-brightgreen

各平台使用的数据源：

- 世嘉 MD/Gensis - `Sega - Mega Drive - Genesis (20240907-224108).dat` 除去 Demo 等：1714；Retool 除去 15 个 promram、1 个 HeartBeat Catalyst，最终：1698
- 世嘉 GameGear - 469 `Sega - Game Gear (20240827-211557)` 812；除去 Demo 等后：469
- 任天堂 GBA - `Nintendo - Game Boy Advance (#3120 + x462).dat` 3562；除去 xXXX、Demo 后：2850
- 任天堂 FC/NES - `Nintendo - Nintendo Entertainment System (Headerless) (20240829-004657).dat` 4170，去除各种后 2247
- 任天堂 N64 - `Nintendo - Nintendo 64 (BigEndian) (20240908-020954).dat` 去掉各种 Demo、Beta 等：962；再用 Retool 去掉 (Wii Virtual Console)，(GameCube)，(LodgeNet) ，(Switch Online)、Wide-Boy64，最后：896 个
