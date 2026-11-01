# 奶娃-众宾欢也

奶蛙桌宠的衍生版：一只变成一群，笑声此起彼伏。

![奶娃桌宠演示：多只奶蛙在桌面散步、大笑](https://cdn.jsdelivr.net/gh/HbS66-pro/naiwa-zhongbinhuanye@main/docs/cover.png)

▶ [完整演示视频（24 秒，带声音）](https://cdn.jsdelivr.net/gh/HbS66-pro/naiwa-zhongbinhuanye@main/docs/demo.mp4) · [动图 GIF](https://cdn.jsdelivr.net/gh/HbS66-pro/naiwa-zhongbinhuanye@main/docs/demo-small.gif)

## 这是什么

基于 [yugh6/Naiwa](https://github.com/yugh6/Naiwa) 改造的 Windows 桌面宠物。
原版是一只坐在屏幕右下角的奶蛙，可以戳肚子、双击大笑、拖着走。
这个版本在它之上加了三件事：

- 戳肚子能把奶蛙越点越大
- 长到最大后会自动分裂出一只新的奶蛙，同屏最多 8 只
- 多只同时大笑时声音叠加，不会互相打断

## 怎么用

1. 到 [Releases](../../releases) 下载最新的压缩包
2. 解压到任意文件夹（路径别带特殊符号）
3. 双击 `奶娃.exe`

右键点奶蛙有菜单：调大小、开关声音、开关全屏隐藏、再来一只、退出。

## 怎么编译

需要 Windows 自带的 .NET Framework 4.x，不需要装 SDK：
```
cd src
build.cmd
```

产物是上一级目录的 `奶蛙桌宠.exe`。要运行它，还需要把 `素材.nwp` 和
`原版笑声.wav` 放到同一目录——这两个文件体积大，没有放进仓库，
从 [Releases](../../releases) 的压缩包里取。

## 和原版的区别

| | 原版 | 本版 |
|---|---|---|
| 奶蛙数量 | 1 只 | 最多 8 只，可分裂 |
| 同时大笑 | 后一只打断前一只 | 各响各的 |
| 单击 | 戳肚子 | 戳肚子 + 长大 |
| 双击 | 大笑 | 大笑，且不改变大小 |

## 许可证

本项目沿用上游的 [PolyForm Noncommercial 1.0.0](LICENCE)：允许非商业用途的使用、修改和分发，禁止商业用途。
原始素材（`素材.nwp`、`原版笑声.wav`）版权归原作者 yugh6。

## 已知限制

- 素材只有一张站立图，走路是程序对腿部做局部变形模拟的，不是真实行走序列帧
- 只在 Windows 10/11 x64 上测过
- 笑声是原版 14 秒的整段音频，多只同时笑时音量会叠加
