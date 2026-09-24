# 自定义刷题 · 题库转换 Skill (quiz-bank-converter)

> 把任意格式的考试资料（PDF 讲义、真题集、Word 文档、表格、笔记、扫描 OCR 文本）一键转换为《自定义刷题》微信小程序标准题库 JSON。
> 支持 WorkBuddy、豆包工作 Agent、DSH、Kimi、网页版 DeepSeek 等主流大模型与智能体。

---

## 🚀 快速使用指南

### 姿势 1：WorkBuddy / 豆包工作 Agent / DSH（直接挂载 GitHub 仓库）

如果你使用的是支持 Agent Skill 规范的工具（如腾讯 WorkBuddy、字节豆包工作台 doubao.com/work、DSH）：
1. 复制本仓库地址：`https://github.com/your-username/custom-quiz-skill`
2. 在工具的「技能 / Skill」管理中直接粘贴该 GitHub 地址完成安装（或直接将 `SKILL.md` 拖入对话框）；
3. 将你的 PDF/Word 题目资料发给 Agent，发送一句话：
   > *"使用《自定义刷题》规范，帮我把这份资料转成题库 JSON，科目是行测，题库名叫专项练习"*
4. Agent 将自动按规范分批提取、补齐字段并输出标准 JSON 文件。

---

### 姿势 2：Kimi / 网页版 DeepSeek / 手机豆包 App（复制提示词即用）

如果你的大模型不支持读取 GitHub 仓库：
1. 打开本仓库的 [`prompt.txt`](./prompt.txt)，复制全部内容；
2. 新建一个对话，把复制的内容粘贴发送给 AI；
3. 将题目文本或 PDF 资料发给 AI，发送：
   > *"开始转换。科目=行测，题库名=真题精选，每批20题"*
4. AI 会按规范分批输出纯 JSON 题目，完成后拼合即可。

---

## 📱 导入小程序开刷

1. 将生成的 `题库名.json` 发送到手机微信「文件传输助手」；
2. 在微信打开「自定义刷题」小程序；
3. 进入「导入」页 → 点击「从微信聊天选择文件」勾选刚刚收到的 JSON 文件；
4. 2秒内自动完成体检并导入入库，立即体验 6 大刷题模式与错题消灭！

---

## 📂 仓库文件说明

- `SKILL.md`：符合 Agent Skill 开放规范的完整元数据、分批协议与六项质量体检规则
- `prompt.txt`：为普通聊天模型定制的一键纯文本提示词
- `example-raw-input.md`：原始题目输入样例
- `example-output.json`：小程序可直接导入的标准题库 JSON 样例
