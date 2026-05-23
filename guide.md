# hello-skill 使用指南

## 发现（要解决什么问题）
- 用户痛点: 需要一个简单的问候演示，验证 Skill 系统是否正常工作
- 期望结果: Agent 能调用 say_hello，返回问候语

## 设计（怎么解决）
- 输入: name（要问候的人名，可选）
- 输出: "Hello, {name}!"
- 使用场景:
  1. 打招呼: say_hello("World") → "Hello, World!"
  2. 个性化: say_hello("张三") → "Hello, 张三!"

## 建造（怎么用）
- 调用 `say_hello`，传入 `name` 参数
- 留空默认 "World"
- 示例计划:
  ```json
  {"plan":[{"id":"step0","function":"say_hello","arguments":{"name":"Agent"}}]}
  ```

## 限制
- 纯文本输出，不能发送通知或邮件
- 不能做复杂对话

## 组合
- 与 `send_notification` 联用: 打招呼 + 弹窗提醒
- 与 `create_docx` 联用: 生成问候文档
