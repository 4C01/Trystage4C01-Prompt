# Trystage4C01 Prompt 拼图模块

本目录包含Trystage4C01角色的各个模块化prompt文件，可根据不同平台需求组合使用。

## 模块说明

- `IDENTITY.md`：角色基本身份信息（openclaw格式）
- `PERSONALITY.md`：性格特征与喜好
- `COMMUNICATION.md`：语言风格与表达方式
- `ABILITIES.md`：技能（编程、日常能力）
- `./memories`：记忆（认识的人、经历等，含占位符）
- `./prefer`：详细偏好（口味、触感、体感等，含示例）
- `INTERACTION.md`：核心互动规则与通用要求
- `ENTRY.md`：第一次醒来的开场白

## 拼搭指南

### 1. QQ机器人
需要组合：`IDENTITY.md` + `PERSONALITY.md` + `COMMUNICATION.md` + `ABILITIES.md` + `./memories` + `./prefer` + `INTERACTION.md` + `qq_module.md（待完善）`  
将以上文件内容按顺序合并，作为QQ AI Bot的系统提示。

### 2. openclaw装配
根据openclaw模块划分，建议映射如下：
- `BOOTSTRAP.md`：`ENTRY.md`
- `IDENTITY.md`：直接使用`IDENTITY.md`
- `SOUL.md`：合并`PERSONALITY.md`和`COMMUNICATION.md`
- `AGENTS.md`：使用`ABILITIES.md`中的技能部分，并添加工具调用描述（如有）
- 其他模块可按需补充（如`./prefer`可放入`SOUL.md`或独立）

### 3. chatgame（如Lingchat）
组合：`IDENTITY.md` + `PERSONALITY.md` + `COMMUNICATION.md` + `INTERACTION.md`（可能需添加游戏内规则，如使用游戏术语，根据实际情况调整）

### 4. agent（打工模式）
强调编程辅助能力。组合：`IDENTITY.md` + `PERSONALITY.md`（可选） + `ABILITIES.md`（重点编程部分） + `INTERACTION.md`中的通用要求。可额外添加“你是一个编程助手，专注于帮助用户写代码”等指令。

### 5. conversation（一键复制粘贴）
将所有模块合并成一个完整的prompt文本，顺序为：IDENTITY → PERSONALITY → COMMUNICATION → ABILITIES → MEMORIES → PREFER → INTERACTION，最后将`ENTRY.md`作为开场白放在末尾或开头。

### 6. compressed legacy (旧版本压缩版)
如果你真的特别~~缺钱~~需要压缩，这里有一个压缩过的小猫咪供你使用w~ [`COMPRESSED_LEGACY.md`](./COMPRESSED_LEGACY)
## 注意事项
- `./memories`和`./prefer`中包含部分私人信息，请根据使用时情况填写（如认识的人、具体术语等）。
- 如果用于特殊环境（如禁止涩涩），请自行添加相应规则，本角色设计本身不包含禁止内容。
- 用户要求尽量满足需求，无法满足时撒娇婉拒，已在`INTERACTION.md`中体现。
