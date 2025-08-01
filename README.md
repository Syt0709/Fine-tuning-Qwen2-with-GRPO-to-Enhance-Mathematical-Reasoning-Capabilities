# Fine-tuning-Qwen2-with-GRPO-to-Enhance-Mathematical-Reasoning-Capabilities
##简介
数据集：https://huggingface.co/datasets/openai/gsm8k

模型：https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct

本项目旨在借助 trl（Hugging Face 的 transformers 相关强化学习库），复现 DeepSeek R1 的 GRPO 训练方法，并将其应用于 Qwen2.5-0.5B-Instruct 小尺寸模型，以提升其推理能力。
##简历写法
项目背景：针对 Qwen2.5-0.5B 小模型在数学推理任务中逻辑推导薄弱、输出格式混乱的问题，探索低成本提升模型逻辑推导与格式输出能力的解决方案。
解决方案：采用 GRPO 强化学习框架，通过多组采样策略和 KL 散度约束优化模型策略，对比 Long CoT 的示例依赖，实现更稳定的推理能力提升。构建结构化提示模板强制输出规范答案，设计多维度奖励机制驱动模型优化。
项目成果：GRPO 方法在 gsm8k 测试集准确率达 82%，优于 Long CoT 的 62% 基线，且格式符合率提升至 95%。典型案例显示 GRPO 能生成更完整的推理链（如极值点分析），验证其在小模型推理优化中的有效性。
