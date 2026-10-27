# Traffic Sign VLM

**基于 Qwen3-VL 的交通标志多模态异常识别与后训练研究。**

[在线展示](https://xyl-0216.github.io/traffic-sign-vlm/) · [GitHub 仓库](https://github.com/xyl-0216/traffic-sign-vlm)

面向交通标志脱落、变形、老化、破坏和污损等异常，研究多模态指令微调、结构化输出与可验证奖励后训练。

## 研究内容

- **指令数据**：样本去重、标签映射与多模态指令组织。
- **参数高效微调**：NF4 量化与 QLoRA，适配 Q/K/V/O 注意力投影。
- **后训练研究**：围绕分类正确性、多标签 F1、格式合法性与标签一致性设计 GRPO 奖励。
- **评测设计**：异常识别、输出可靠性以及训练和推理资源开销。

## 项目展示

网站包含训练方法、奖励组成与五类异常的交互示例。图像和 JSON 为任务示意，不作为模型实测结果。

```text
site/
  index.html   展示页面
  style.css    响应式样式
  app.js       训练流程、奖励设计和异常示例交互
.github/workflows/pages.yml   GitHub Pages 自动发布
```

页面无需前端构建依赖，可直接打开 `site/index.html`。推送到 `main` 后，GitHub Actions 自动发布 `site/`。

## 相关项目

[Prism Research](https://github.com/xyl-0216/prism-research)：多模态研究 Agent，支持证据检索、研究规划和来源追溯。

## 许可

本仓库前端代码以 [MIT License](LICENSE) 分发。Qwen3-VL 等上游模型及后续引入的第三方组件遵循各自许可。
