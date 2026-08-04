# Survey Papers by Technical Paradigm

这个清单把主文中的代表论文按四种技术范式整理，便于后续继续补充 DOI、venue、正式 arXiv 链接和 BibTeX 元数据。当前口径来自 [../survey.tex](../survey.tex) 的四范式章节、[../paper-matrix.md](../paper-matrix.md) 的 seed matrix，以及 [../references.bib](../references.bib) 的题名/年份/链接字段。

分类逻辑：

| 范式 | 视觉角色 | 判断标准 |
| --- | --- | --- |
| 范式 1: 隐空间想象 | 视觉作为压缩透镜 | 先把像素压成 latent/belief，再在 latent 中做 rollout、value、search 或 MPC |
| 范式 2: 响应式 VLA | 视觉作为语义骨干 | 图像/视频与语言被映射到 action token 或技能，通常不显式生成多步未来 |
| 范式 3: 动作条件视频仿真 | 视觉作为动力学引擎 | action、route、camera 或 latent control 条件化未来视频/可交互帧 |
| 范式 4: 视觉世界动作模型 | 视觉与动作共生/协同生成 | 未来视觉状态和动作轨迹在一个 joint visual-action space 中生成、约束或互相校正 |

## 范式 1: 隐空间想象

视觉作为“压缩透镜”：camera pixels -> visual latent/belief -> latent dynamics/search/MPC/policy learning。

| Paper title | 链接 | 时间 | 方向/关键词 |
| --- | --- | --- | --- |
| [TD-MPC2: Scalable, Robust World Models for Continuous Control](https://scholar.google.com/scholar?q=TD+MPC2+Scalable+Robust+World+Models+for+Continuous+Control) | Scholar | 2024 | latent dynamics, MPC, continuous control, robotics |
| [Mastering Diverse Domains through World Models](https://scholar.google.com/scholar?q=Mastering+Diverse+Domains+through+World+Models) | Scholar | 2023 | DreamerV3, RSSM, actor-critic, scalable latent imagination |
| [Mastering Atari with Discrete World Models](https://scholar.google.com/scholar?q=Mastering+Atari+with+Discrete+World+Models) | Scholar | 2021 | DreamerV2, discrete latent state, Atari, policy learning |
| [Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model](https://scholar.google.com/scholar?q=Mastering+Atari+Go+Chess+and+Shogi+by+Planning+with+a+Learned+Model) | Scholar | 2020 | MuZero, implicit latent dynamics, MCTS, reward/value/policy prediction |
| [Dream to Control: Learning Behaviors by Latent Imagination](https://scholar.google.com/scholar?q=Dream+to+Control+Learning+Behaviors+by+Latent+Imagination) | Scholar | 2020 | Dreamer, latent rollout, reward/value learning, control from pixels |
| [Learning Latent Dynamics for Planning from Pixels](https://scholar.google.com/scholar?q=Learning+Latent+Dynamics+for+Planning+from+Pixels) | Scholar | 2019 | PlaNet, RSSM, planning from pixels, sample-efficient control |
| [World Models](https://scholar.google.com/scholar?q=World+Models) | Scholar | 2018 | VAE, MDN-RNN, latent rollout, game agents |

## 范式 2: 响应式 VLA

视觉作为“语义骨干”：image/video + language -> semantic/action tokens -> next action or skill。

| Paper title | 链接 | 时间 | 方向/关键词 |
| --- | --- | --- | --- |
| [OpenVLA: An Open-Source Vision-Language-Action Model](https://scholar.google.com/scholar?q=OpenVLA+An+Open+Source+Vision+Language+Action+Model) | Scholar | 2024 | open-source VLA, VLM grounding, robot action tokens |
| [Octo: An Open-Source Generalist Robot Policy](https://scholar.google.com/scholar?q=Octo+An+Open+Source+Generalist+Robot+Policy) | Scholar | 2024 | generalist robot policy, multitask transformer, multimodal observation |
| [RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://scholar.google.com/scholar?q=RT+2+Vision+Language+Action+Models+Transfer+Web+Knowledge+to+Robotic+Control) | Scholar | 2023 | VLA, VLM-to-action transfer, web knowledge, robot manipulation |
| [PaLM-E: An Embodied Multimodal Language Model](https://scholar.google.com/scholar?q=PaLM+E+An+Embodied+Multimodal+Language+Model) | Scholar | 2023 | embodied multimodal LM, VLM grounding, robotics reasoning |
| [RT-1: Robotics Transformer for Real-World Control at Scale](https://scholar.google.com/scholar?q=RT+1+Robotics+Transformer+for+Real+World+Control+at+Scale) | Scholar | 2022 | robot transformer, imitation learning, language-conditioned actions |

## 范式 3: 动作条件视频仿真

视觉作为“动力学引擎”：action/control/route/camera path -> future video tokens or playable frames。

| Paper title | 链接 | 时间 | 方向/关键词 |
| --- | --- | --- | --- |
| [ChronoDreamer: Action-Conditioned World Model as an Online Simulator for Robotic Planning](https://scholar.google.com/scholar?q=ChronoDreamer+Action+Conditioned+World+Model+as+an+Online+Simulator+for+Robotic+Planning) | Scholar | 2025 | robotics planning, action-conditioned simulator, online rollout |
| [Video Generation Models as World Simulators](https://scholar.google.com/scholar?q=Video+Generation+Models+as+World+Simulators) | Scholar | 2024 | Sora, visual world simulator, video diffusion/transformer, controllability |
| [Genie: Generative Interactive Environments](https://scholar.google.com/scholar?q=Genie+Generative+Interactive+Environments) | Scholar | 2024 | interactive video, latent actions, controllable generated worlds |
| [Diffusion Models Are Real-Time Game Engines](https://scholar.google.com/scholar?q=Diffusion+Models+Are+Real+Time+Game+Engines) | Scholar | 2024 | GameNGen, action-conditioned game frames, real-time neural engine |
| [GAIA-1: A Generative World Model for Autonomous Driving](https://scholar.google.com/scholar?q=GAIA+1+A+Generative+World+Model+for+Autonomous+Driving) | Scholar | 2023 | driving world model, video/action/text latent, scene simulation |
| [DriveDreamer: Towards Real-world-driven World Models for Autonomous Driving](https://scholar.google.com/scholar?q=DriveDreamer+Towards+Real+world+driven+World+Models+for+Autonomous+Driving) | Scholar | 2023 | autonomous driving, diffusion, HD map/3D box control, video simulation |
| [DrivingDiffusion: Layout-Guided Multi-View Driving Scene Video Generation with Latent Diffusion Model](https://scholar.google.com/scholar?q=DrivingDiffusion+Layout+Guided+Multi+View+Driving+Scene+Video+Generation+with+Latent+Diffusion+Model) | Scholar | 2023 | multi-view driving video, layout guidance, latent diffusion |
| [Learning Interactive Real-World Simulators](https://scholar.google.com/scholar?q=Learning+Interactive+Real+World+Simulators) | Scholar | 2023 | UniSim, interactive real-world simulation, action-conditioned generation |
| [VideoGPT: Video Generation using VQ-VAE and Transformers](https://scholar.google.com/scholar?q=VideoGPT+Video+Generation+using+VQ+VAE+and+Transformers) | Scholar | 2021 | video tokenization, autoregressive transformer, future video prediction |
| [Learning to Simulate Dynamic Environments with GameGAN](https://scholar.google.com/scholar?q=Learning+to+Simulate+Dynamic+Environments+with+GameGAN) | Scholar | 2020 | game simulation, memory, controllable video dynamics |
| [Visual Foresight: Model-Based Deep Reinforcement Learning for Vision-Based Robotic Control](https://scholar.google.com/scholar?q=Visual+Foresight+Model+Based+Deep+Reinforcement+Learning+for+Vision+Based+Robotic+Control) | Scholar | 2018 | robotic visual foresight, video prediction, MPC |
| [Action-Conditional Video Prediction using Deep Networks in Atari Games](https://scholar.google.com/scholar?q=Action+Conditional+Video+Prediction+using+Deep+Networks+in+Atari+Games) | Scholar | 2015 | Atari, action-conditioned prediction, visual dynamics |

## 范式 4: 视觉世界动作模型

视觉与动作“共生/协同生成”：goal/history -> interleaved visual-action tokens or joint diffusion -> future features and executable action trajectories。

| Paper title | 链接 | 时间 | 方向/关键词 |
| --- | --- | --- | --- |
| [WorldDiT: A Unified Diffusion Architecture for World and Action Modeling](https://arxiv.org/abs/2607.23909) | arXiv | 2026 | unified diffusion, world/action modeling, joint visual-action generation |
| [T-TWAM: Scaling Tactile-Native World-Action Model for Contact-Rich Manipulation](https://arxiv.org/abs/2607.23783) | arXiv | 2026 | tactile-native WAM, contact-rich manipulation, robotics |
| [Masked Visual Actions for Unified World Modeling](https://arxiv.org/abs/2607.19343) | arXiv | 2026 | masked visual actions, unified world modeling, visual-action tokens |
| [GeoWorldAD: Geometry World Action Model for Autonomous Driving](https://arxiv.org/abs/2607.17521) | arXiv | 2026 | geometry-grounded WAM, autonomous driving, world-action modeling |
| [BadWAM: When World-Action Models Dream Right but Act Wrong](https://arxiv.org/abs/2607.15207) | arXiv | 2026 | WAM failure analysis, action feasibility, verification |
| [Qwen-RobotWorld: Unifying Embodied World Modeling through Language-Conditioned Video Generation](https://arxiv.org/abs/2606.17030) | arXiv | 2026 | embodied world modeling, language-conditioned video, robotics |
| [HarmoWAM: Harmonizing Generalizable and Precise Manipulation via Adaptive World Action Models](https://arxiv.org/abs/2605.10942) | arXiv | 2026 | adaptive WAM, manipulation, generalization and precision |
| [Cosmos 3: Omnimodal World Models for Physical AI](https://scholar.google.com/scholar?q=Cosmos+3+Omnimodal+World+Models+for+Physical+AI) | Scholar | 2026 | omnimodal physical AI, world model foundation system, visual-action grounding |
| [NVIDIA OmniDreams: Real-Time Generative World Model for Closed-Loop Autonomous Vehicle Simulation](https://scholar.google.com/scholar?q=NVIDIA+OmniDreams+Real+Time+Generative+World+Model+for+Closed+Loop+Autonomous+Vehicle+Simulation) | Scholar | 2026 | real-time generative world model, closed-loop driving simulation |
| [GeoSem-WAM: Geometry- and Semantic-Aware World Action Models](https://scholar.google.com/scholar?q=GeoSem+WAM+Geometry+and+Semantic+Aware+World+Action+Models) | Scholar | 2026 | geometry/semantic WAM, physical AI, executable futures |
| [CLAW: Learning Continuous Latent Action World Models via Adversarial Latent Regularization](https://scholar.google.com/scholar?q=CLAW+Learning+Continuous+Latent+Action+World+Models+via+Adversarial+Latent+Regularization) | Scholar | 2026 | continuous latent action, adversarial regularization, WAM |
| [OSCAR: Omni-Embodiment Skeleton-Conditioned World Action Model for Robotics](https://scholar.google.com/scholar?q=OSCAR+Omni+Embodiment+Skeleton+Conditioned+World+Action+Model+for+Robotics) | Scholar | 2026 | omni-embodiment, skeleton-conditioned WAM, robotics |
| [WorldRFT: Latent World Model Planning with Reinforcement Fine-Tuning for Autonomous Driving](https://scholar.google.com/scholar?q=WorldRFT+Latent+World+Model+Planning+with+Reinforcement+Fine+Tuning+for+Autonomous+Driving) | Scholar | 2025 | latent world model planning, reinforcement fine-tuning, autonomous driving |
| [Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://scholar.google.com/scholar?q=Diffusion+Policy+Visuomotor+Policy+Learning+via+Action+Diffusion) | Scholar | 2023 | action diffusion, visuomotor policy, trajectory generation, WAM precursor |
| [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://scholar.google.com/scholar?q=Learning+Fine+Grained+Bimanual+Manipulation+with+Low+Cost+Hardware) | Scholar | 2023 | ACT, action chunking, imitation learning, robot action sequence modeling |

## 维护规则

- 每个范式内部按年份倒排；同一年优先放主文中更靠近该范式定义的代表系统。
- 如果论文横跨多个范式，放到其在 survey 论证中承担的主要角色；例如 Diffusion Policy 同时是 action generation 基础，但在这里作为 WAM precursor。
- 新增论文时至少补齐四列：`Paper title`、`链接`、`时间`、`方向/关键词`。
- 后续 camera-ready 前建议把 Scholar 链接替换为正式 DOI、OpenReview、arXiv 或项目页链接。
