# 本账号的上游自动同步说明

- 本仓库：<https://github.com/mengfanghua3-max/ai-ref-library-cn>
- 原作者仓库：<https://github.com/sleepy-zone/ai-ref-library-cn>
- 自动任务：[Sync upstream](https://github.com/mengfanghua3-max/ai-ref-library-cn/actions/workflows/mfh-sync-upstream.yml)

每 6 小时检查并合并上游。计划时间为北京时间 02:17、08:17、14:17、20:17；GitHub 调度可能延迟。也可以进入上面的 Actions 页面，点击 **Run workflow** 手动同步。

同步使用 GitHub 内置的临时 GITHUB_TOKEN，只授予本仓库内容写权限。不会强制覆盖分支；发生合并冲突或权限错误时任务失败，保留当前内容，由维护者查看运行日志处理。工作流不下载执行上游脚本，不保存个人访问令牌。

公开仓库连续 60 天没有活动时，GitHub 可能停用定时工作流。因此，成功同步后如发现仓库已连续 45 天没有 push，任务会写入一次 `.github/mfh-sync-activity.json`，记录检查时间及上游版本；有近期活动时不额外提交。这是低频维护措施，不能保证 GitHub 调度服务永远不暂停。若显示 Disabled，请重新启用本工作流；若显示 Failure，请查看错误信息，不要强制覆盖。

这是代码与仓库中现有素材的同步，不等于全量原图备份，也不会自动升级本机的澜姿。仓库内原图下载入口仍可能依赖原站服务；使用素材请查看原作者规则。未来上游新增工作流文件如触发权限限制，需要另行处理。

三个原站已单独保存为网址收藏：

- [脸库收藏](https://github.com/mengfanghua3-max/ai-portrait-gallery-bookmark)
- [姿势库收藏](https://github.com/mengfanghua3-max/ai-pose-gallery-bookmark)
- [服装库收藏](https://github.com/mengfanghua3-max/ai-costume-gallery-bookmark)

GitHub 规则参考：[同步 Fork](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork)、[启用和停用工作流](https://docs.github.com/en/actions/how-tos/manage-workflow-runs/disable-and-enable-workflows)。
