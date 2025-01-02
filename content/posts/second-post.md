+++
date = '2025-01-02T23:17:52+08:00'
draft = true
title = 'Second Post'
+++
>[! Tip] 要求以 `Tag` 开头，方便分类以及后续回顾。

---

-  #论文 有没有可能，提到的启发式方法和 MRAT 里面的启发式方法是同一种方法？
- #论文 1. 逃逸者速度考虑是否和追击者持平/更大？2. Large 那篇论文如果只从追击者的角度考虑，其实就是一个 PPO，因为所有追击机器人策略共享。3. 状态输入和奖励函数要和我的文章保持一致，因为这些是针对特定场景的优化结果。
---

2024-12-28

#llm LLM 原理相关资料：
- https://github.com/datawhalechina/so-large-lm?tab=readme-ov-file 原理部分
- https://github.com/datawhalechina/self-llm 应用部分
---

2024-12-31

#论文  策略网络时单独实现的，具体的训练是在 `Agent` 类中，新建一个函数 `train_mix_attention` / `train_ppo` 等，然后在 `agent:train()` 方法中调用，`agent.train()` 在 `trainer.learn()` 中调用。

---

2025-01-02

#论文

写论文的时候可以突出以下几点：
- 不需要知道环境的所有信息，局部观测+所有目标信息；不需要知道全局信息，也不需要建图
- 不受数量限制
- 围捕难度更大
- 运动模型更加符合实际

需要提一下 baseline 论文是追击问题，我们这里稍作改动。