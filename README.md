# AIConnector Relay

这里是 [AIConnector](https://github.com/Kirrito-k423/AIConnector) 的专用公开运行仓库，由程序维护任务和交付件。

- 一项任务一个 Issue：`[AIC][task_id] 任务标题`。同一任务的修订、重跑都保留在原 Issue。
- 一次运行一个 Release：`aic-v1.experiments-v1.<task_id>.r<revision>.<run_id>`。
- 状态用追加评论：任务 → 已接收 → 已领取 → 结果 → 回执。
- 输入 ZIP：`input--mac-outer--<SHA256>.zip`；结果 ZIP：`result--windows-inner--<SHA256>.zip`。
- 每个 ZIP 小于 5 MiB；协议载荷给出字节数、SHA-256 和稳定下载链接。

[查看任务](https://github.com/Kirrito-k423/AIConnector-Relay/issues?q=is%3Aissue) · [查看运行文件](https://github.com/Kirrito-k423/AIConnector-Relay/releases) · [完整格式与恢复规则](https://github.com/Kirrito-k423/AIConnector/blob/v0.3.0-rc.1/docs/RELAY.md)

普通评论、标题、标签和 Issue 开关不触发执行。`started` 表示持久化领取；`receipt` 表示交付件完整收到；它们不证明实验实际启动或验收通过。修改协议评论或固定登记正文会触发冲突检查。

软件缺陷与安装包留在代码仓库。本仓库不存实验源码，不依赖内网 Git clone/push。任务说明和 ZIP 均公开；凭据只留在运行机器上。

仓库声明见 [.aiconnector/relay.json](.aiconnector/relay.json)。时间线记录保留在 Issue 评论和两端本地状态；不要删除活跃任务的 Issue、Release 或状态目录。
