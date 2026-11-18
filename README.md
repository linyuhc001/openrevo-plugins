# OpenRevo 插件集（linyuhc001）

面向 [OpenRevo](https://github.com/faintonce/open-revo) 的两个第三方插件，按 `openrevo-plugin` topic 收录进[插件市场](https://github.com/LIPiston/open-revo-market)。

## 插件列表

| 插件 | 目录 | 版本 | 说明 |
|---|---|---|---|
| PBO 精准调校 (SMU Debug) | `pbo-tuner/` | 2.0.0 | AMD Ryzen PBO / SMU 调校（自带伴随服务） |
| 进程管理 | `process-manager/` | 1.6.0 | 进程 / 连接端口 / 文件占用三合一检视（自带伴随服务） |

## 重要声明

- **两者都带提权伴随服务（`elevated: true`）**，以管理员上下文运行：
  - `pbo-tuner` 依赖 [PawnIO](https://pawnio.eu/) 内核驱动直连 SMU；使用前须先安装 PawnIO。
  - `process-manager` 使用 Restart Manager 通道管理进程与文件占用。
- 插件直接作用于硬件固件 / 系统进程，请理解参数含义后再操作。PBO 插件仅建议用于写入已调好的参数，不用于自行摸索负压。
- 本仓库的插件以你的权限运行，请自行判断是否信任。

## 上架

仓库根打 `openrevo-plugin` topic 后，市场爬虫会在约一小时内收录两个一级子目录。收录条目自动标记为「未审核」。

## 宿主版本

- pbo-tuner: 最低 OpenRevo 0.9.7
- process-manager: 最低 OpenRevo 0.9.4
