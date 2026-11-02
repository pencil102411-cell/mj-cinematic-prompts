# 给视频当首帧／分镜图

用户要用 MJ 出的图当视频模型的第一帧或开场构图参考（MV、短剧分镜图、"首帧图"）时读本文件。这张图要按"视频的第一帧"写，不是按海报写。以下规律来自 2026-10-29~30 一支 MV 的实战（MJ 出图 → 本地 H3 / Seedance 生成），是实测观察，不保证每次复现。

## 构图就是开场

- **景别就是视频开场的景别**：视频模型会照搬这张图的景别和站位。要胸口以上近景就写 `chest-up close-up`；写成半身海报，视频前一两秒就是半身。
- **姿势是动作开始之前的那一刻**：要她抬眼就写低着眼（`eyes lowered`）；要拉下墨镜，手已经搭在墨镜上（`fingertips already on the sunglasses pushed up on her head`）。不要写动作做完的样子。
- **位置写死**：人在画面哪一侧、占多大、朝哪边，例如 `standing in the left third of the frame, body turned toward frame right, about to walk`。只写 `walking` 时位置和方向常常不对。
- **群众写成在做事**：`people in the queue chatting to each other, laughing, not looking at the camera`；要他们拍人就写 `holding their phones up, filming toward frame right`。只写 `a queue of people` 容易出成低头玩手机或齐刷刷盯镜头。

## 正顶俯拍

- `top-down` / `overhead` 常被出成高处斜着往下看。写成 `drone shot pointing straight down at 90 degrees, no horizon, no walls visible, the floor fills the whole frame`。
- 要视频拍出正顶俯拍有人的画面，图里最好已经有从头顶看下去的人；空的俯拍场景交给视频模型，它可能照人物参考图的正面站姿出成正面。

## 不要的东西

- **字**：招牌、门牌、EXIT、楼层号、数字会被视频模型变成乱码。正文用正面描述去掉字的来源，比如 `blank unmarked concrete walls, plain pillars`，别写 `no text`（否定词 MJ 常读不懂，反而可能画出来）；出图后有字就裁掉或擦掉再用。
- **人**：空场景、给多人生成用的场景图，正文强调 `completely empty of people`，否则常自己加人。
- **画面外的东西别写**：近景里写地面、脚下的灯，图会为了拍到地面变宽，视频也跟着变成全身。
- **专属细节的左右**：人物某侧脸上有记号（痣、小红心）时写明哪一侧；出过把记号画到另一侧的情况，出图后对照设定图检查。

## 出图后

- MJ 常加上下黑边：用之前裁掉。比 16:9 更宽的图别硬裁成 16:9 切掉人，可以上下补窄黑边。
- 图里替身的脸不会被参考生视频带走（脸以人物设定图为准），所以挑图时优先看**构图、光、姿势、有没有字**，脸像不像次要。
- 用户通常每刀出 2~4 张、挑 2 张放进文件夹，再由 Claude 按上面几条选一张并写下理由。
