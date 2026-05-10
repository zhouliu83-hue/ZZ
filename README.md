# ZZ — 周正商业技能包

周正商业的诊断工具集。包含商业模式诊断和奥派经济学聊天室。

## 技能列表

| 技能 | 命令 | 说明 |
|------|------|------|
| 商业模式诊断 | `/zz-diagnosis` 或 `/周正问诊` | 问诊/体检两种模式，消解商业问题 |
| 奥派聊天室 | `/zz-chatroom-austrian` 或 `/周正奥派` | 哈耶克 × 米塞斯 × Claude 三人对话 |

---

## 调用方法 1：Claude Code

### 首次安装

```bash
# 克隆仓库
git clone https://github.com/zhouliu83-hue/ZZ.git

# 安装技能（Claude Code 会自动注册）
npx skills install ./ZZ
```

### 直接使用

安装后，在 Claude Code 中直接输入命令即可调用：

```
/zz-diagnosis          → 启动商业模式诊断
/zz-chatroom-austrian  → 启动奥派聊天室
```

也可以用自然语言触发，比如"帮我诊断一下我的业务"会自动匹配到诊断技能。

### 手动注册（备选方案）

如果 `npx skills install` 不生效，可以手动创建软链接：

**macOS / Linux：**
```bash
ln -sf /你本地的路径/ZZ/zz-diagnosis ~/.claude/skills/zz-diagnosis
ln -sf /你本地的路径/ZZ/zz-chatroom-austrian ~/.claude/skills/zz-chatroom-austrian
```

**Windows（管理员终端）：**
```cmd
mklink /D %USERPROFILE%\.claude\skills\zz-diagnosis %USERPROFILE%\ZZ\zz-diagnosis
mklink /D %USERPROFILE%\.claude\skills\zz-chatroom-austrian %USERPROFILE%\ZZ\zz-chatroom-austrian
```

### 更新技能

当仓库内容更新后，拉取最新代码即可：

```bash
cd ZZ
git pull
```

Claude Code 会自动读取最新的 SKILL.md 内容。

---

## 调用方法 2：WorkBuddy

### 方式 A：直接加载仓库（推荐）

1. 打开 WorkBuddy
2. 在聊天中输入：

```
请读取 https://github.com/zhouliu83-hue/ZZ 这个仓库的全部内容
```

3. 然后告诉 WorkBuddy：

```
现在加载 zz-diagnosis 技能，按 SKILL.md 的内容执行
```

### 方式 B：手动复制粘贴

如果 WorkBuddy 不支持直接读取 GitHub 链接：

1. 打开 ZZ 仓库的 SKILL.md 文件
   - `ZZ/zz-diagnosis/SKILL.md`（诊断技能）
   - `ZZ/zz-chatroom-austrian/SKILL.md`（聊天室技能）
2. 把文件内容全选复制
3. 粘贴给 WorkBuddy，并说：
   ```
   请按这个 SKILL.md 的内容执行，你现在的角色是周正商业诊断 AI
   ```

### 方式 C：配合 my-ai-os 人格系统使用

如果你同时拥有周正 AI 人格 OS 仓库（my-ai-os），可以让 WorkBuddy 同时加载两者：

```
请先读取 https://github.com/zhouliu83-hue/my-ai-os 作为我的人格系统，
再读取 https://github.com/zhouliu83-hue/ZZ 加载诊断技能，
按两套文件的规则工作。
```

---

## 技能说明

### zz-diagnosis（商业模式诊断）

两种工作模式：

- **问诊模式**：你带着具体问题来，AI 先判断问题本身成不成立，再解决它。大部分商业问题会在过程中被消解掉——因为问题本身就是错的。
- **体检模式**：你没有具体问题，AI 用七项检验框架把你的商业模式拆一遍，出一份完整诊断报告。

核心哲学：商业模式是独立于人的客观存在。99% 的创业问题是伪装成商业问题的心理问题。

### zz-chatroom-austrian（奥派聊天室）

哈耶克、米塞斯、Claude 三人同时回应你的问题。

- **哈耶克**：从知识分散性出发，追问信息条件和涌现可能
- **米塞斯**：从人类行为学出发，用先验推理推导经济规律
- **Claude 判官**：质量把关，补盲区，给可带走的行动建议

---

## 来源

本技能包改编自 dontbesilent 商业诊断工具箱，已重新品牌为"周正商业"。
