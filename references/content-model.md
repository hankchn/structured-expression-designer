# 统一内容模型

在画图前，把原始内容整理为以下结构。字段可以省略，但不要凭空补全。

```yaml
objective:
  question: 核心要回答的问题
  audience: 阅读对象
  context: 使用场景
  takeaway: 希望读者记住或采取的行动

content:
  entities:
    - id:
      label:
      type:
      description:
  relationships:
    - from:
      to:
      type: sequence | branch | ownership | hierarchy | cause | dependency | comparison
      label:
  groups:
    - name:
      members: []
  stages:
    - name:
      order:
      goal:
  metrics:
    - name:
      value:
      unit:
      period:
      source:

evidence:
  facts: []
  inferences: []
  hypotheses: []
  placeholders: []

presentation:
  emphasis:
  density: low | medium | high
  editable_format:
  constraints:
```

## 抽取步骤

1. 删除重复、寒暄和不影响表达的细节。
2. 抽取名词作为对象，动词作为关系。
3. 识别主线、分支、层级、时间、责任和数据。
4. 合并同义对象，统一命名。
5. 将长句压缩为“动作 + 对象”或“结论 + 证据”。
6. 把未知信息放入 `placeholders`，不要自行编造。
7. 检查每个节点是否服务于核心问题。

## 信息不足时

只有缺失内容会改变图形类型或产生事实风险时才询问用户。优先询问：

- 核心读者是谁？
- 最重要的结论是什么？
- 时间、角色、数据或因果是否真实存在？
- 需要哪种二次编辑格式？

若可以合理继续，则用明确占位符生成草稿，并列出待补信息。

## 内容压缩规则

- 流程节点：2-10 个汉字为宜。
- 一级分组：通常 3-7 个。
- 单张汇报图：主要节点通常不超过 12 个。
- 全景图：一级分组不超过 6 个，每组内部保持同一粒度。
- 数据图：标题直接写结论，图中不重复整段分析。

