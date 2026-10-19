# text-digest

一个最小可用的 WorkBuddy Skill：把长文本压成结构化摘要。

## 结构

```
skills/text-digest/SKILL.md   # 技能定义（触发条件 / 输入 / 步骤 / 输出 / 调用示例）
```

## 安装

把 `skills/text-digest/` 复制到 `~/.workbuddy/skills/` 下即可。

## 设计要点

- `description` 同时声明适用与不适用场景，减少误触发
- 只有 `text` 为必填，其余参数缺失时取默认值，不追问
- 输出固定四段：结论 / 要点 / 关键数字 / 待确认，无内容整段省略
- 每条断言必须在原文可定位，否则删除
