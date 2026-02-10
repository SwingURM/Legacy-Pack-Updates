# Legacy Pack Updates

用于改进旧模组整合包（使用更新后的模组）的说明集合。

## 关于本补丁

本仓库提供 FTB Infinity Evolved Skyblock 的配置补丁。

由于未获得 FTB 团队明确许可，**本仓库不包含**其配置文件。

### 包含的改动

- 采用 glowredman's 所有配置修改建议（除 EnderIO 语言文件外）
- 添加钻石合成配方：由 1 颗钻石合成 9 个 Magic Bees 钻石颗粒
  - *原因*：Magic Bees 将钻石颗粒注册为钻石粒的词典，导致 Agricraft 放弃了自己的钻石粒注册和配方，但 Magic Bees 自身没有添加由钻石合成钻石颗粒的配方，破坏了钻石粒与压缩抽屉的原有互动
- 禁用 chisel aeskystone 配置（在近期测试版本中无法启动）
- 禁用 Hodgepodge 的 eventbus配置项（InpureCore）(https://github.com/GTNewHorizons/Hodgepodge/issues/627)

其余所有新增配置均为自动生成的新配置项。部分配置（如 NEI 物品组合并）参考自 GTNH 模组包，非常感谢 GTNH 社区的贡献。

### 使用方法

1. 从 Curse 下载 FTB Infinity Evolved Skyblock 整合包
2. 解压后进入 `overrides` 文件夹
3. 初始化 git 仓库并提交当前状态：

   ```bash
   git init
   git add .
   git commit -m "Initial"
   ```

4. 应用补丁：

   ```bash
   git apply /path/to/patch.patch
   ```

## 模组获取

本仓库不包含模组文件。新版模组的下载器可从 [DreamAssemblerXXL (fork)](https://github.com/SwingURM/FTB-Infinity-Evolved-Skyblock-Assmbler) 获取。

**注意**：当前版本需要 GitHub 和 Curse 的 token 才能使用，且 Curse 无法下载 FTB-Trophy 和 Decocraft，需手动操作。

## 已知问题

- **硅蜜蜂被禁用**：Magic Bees 改用是否存在硅粉来决定硅蜜蜂是否生成，导致硅蜜蜂及后续的 Infinity 蜂等被禁用。解决方案尚未确定（可能需创建补丁模组或 fork Magic Bees）
- **Infinity 蜂双路线**：修复上述问题后，存在两条杂交路线可通往最终的 Infinity 蜂，原因不明
- **Ex Nihilo 筛子进度异步**：最新 release 版本的 3x3 筛子进度不同步
- **Ex Nihilo 石桶可无限添加固体**: 最新release下石桶可超出容量地不断加入石头
