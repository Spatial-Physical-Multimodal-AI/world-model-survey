# Awesome World Models: From Reaction to Imagination

![papers](https://img.shields.io/badge/papers-115-blue) ![topic](https://img.shields.io/badge/topic-world--models-green) ![scope](https://img.shields.io/badge/scope-reaction--to--imagination-orange)

A curated reading list accompanying *From Reaction to Imagination: A Survey on World Models*.

[PDF](../build/world-model-survey-v1.pdf) · [LaTeX](../survey-v1.tex) · [Quality report](../autoresearch/quality_report_v1.md)

本列表采用 v1 的 operational boundary：agent-facing world model 必须同时具备 interactivity 与 predictive imagination。VLM 和多数 reactive VLA 是重要基线；严格 world model 按主要接口分为 Latent WM、Vision WM 和 WAM。

## Table of Contents

- [Taxonomy Map](#taxonomy-map)
- [General Surveys and Position Papers](#general-surveys-and-position-papers)
- [Baseline: Reactive VLA](#baseline-reactive-vla)
- [Family 1: Latent World Models](#family-1-latent-world-models)
- [Family 2: Vision World Models](#family-2-vision-world-models)
- [Family 3: World Action Models](#family-3-world-action-models)
- [Autonomous Driving and 3D/BEV World Models](#autonomous-driving-and-3dbev-world-models)
- [Digital Agents and Verification](#digital-agents-and-verification)
- [Maintenance Notes](#maintenance-notes)

## Taxonomy Map

| Class | Agent-facing interface | Predictive imagination | Core question |
| --- | --- | --- | --- |
| Baseline: VLM | observation/language -> semantics | None by default | What does the current scene mean? |
| Baseline: Reactive VLA | observation/language -> action | Implicit or unexposed | Can the policy act without comparing inspectable futures? |
| Family 1: Latent WM | action-conditioned latent/belief transition | Implicit in compressed state | What must survive compression for planning? |
| Family 2: Vision WM | action-conditioned pixels/video/BEV/occupancy | Explicit visual or geometric future | Is the rendered future physically usable? |
| Family 3: WAM | joint future-state/action generation | Explicit and action-coupled | Can imagined futures and actions constrain each other? |

## General Surveys and Position Papers

_Direction / keywords: Survey / taxonomy / field mapping_

- World Models: A Comprehensive Survey of Architectures, Methodologies, Reasoning Paradigms, and Applications, 2026 [[paper]](https://scholar.google.com/scholar?q=World+Models+A+Comprehensive+Survey+of+Architectures+Methodologies+Reasoning+Paradigms+and+Applications) _Survey / taxonomy / field mapping_
- World Models for Robotic Manipulation: A Survey, 2026 [[paper]](https://scholar.google.com/scholar?q=World+Models+for+Robotic+Manipulation+A+Survey) _Survey / taxonomy / field mapping_
- From Human Videos to Robot Manipulation: A Survey on Scalable Vision-Language-Action Learning with Human-Centric Data, 2026 [[paper]](https://arxiv.org/abs/2606.00054) _Survey / taxonomy / field mapping_
- Model-Based Reinforcement Learning: A Survey, 2023 [[paper]](https://scholar.google.com/scholar?q=Model+Based+Reinforcement+Learning+A+Survey) _Survey / taxonomy / field mapping_

## Baseline: Reactive VLA

_Direction / keywords: VLA / robot policy / semantic grounding / action tokens_

- Pre-VLA: Preemptive Runtime Verification for Reliable Vision-Language-Action and World-Model Rollouts, 2026 [[paper]](https://arxiv.org/abs/2605.22446) _VLA / robot policy / semantic grounding / action tokens_
- PiL-World: A Chunk-Wise World Model for VLA Policy-in-the-Loop Evaluation, 2026 [[paper]](https://arxiv.org/abs/2606.05773) _VLA / robot policy / semantic grounding / action tokens_
- MemoryVLA++: Temporal Modeling via Memory and Imagination in Vision-Language-Action Models, 2026 [[paper]](https://arxiv.org/abs/2606.09827) _VLA / robot policy / semantic grounding / action tokens_
- MPCoT: Reward-Guided Multi-Path Latent Reasoning for Test-Time Scalable Vision-Language-Action, 2026 [[paper]](https://arxiv.org/abs/2606.06245) _VLA / robot policy / semantic grounding / action tokens_
- Intercepting the Future: Latent-Space Predictive World Model for Dynamic VLA Manipulation, 2026 [[paper]](https://scholar.google.com/scholar?q=Intercepting+the+Future+Latent+Space+Predictive+World+Model+for+Dynamic+VLA+Manipulation) _VLA / robot policy / semantic grounding / action tokens_
- HyWorldVLA: A Vision-Language-Action Model with Hybrid World Modeling for Autonomous Driving, 2026 [[paper]](https://arxiv.org/abs/2607.20988) _VLA / robot policy / semantic grounding / action tokens_
- GeoAlign: Beyond Semantics with State-Guided Spatial Alignment in VLA Models, 2026 [[paper]](https://scholar.google.com/scholar?q=GeoAlign+Beyond+Semantics+with+State+Guided+Spatial+Alignment+in+VLA+Models) _VLA / robot policy / semantic grounding / action tokens_
- FoMoVLA: Bridging Visual Foresight and Motion Guidance for Vision-Language-Action Models, 2026 [[paper]](https://arxiv.org/abs/2607.14739) _VLA / robot policy / semantic grounding / action tokens_
- CheckVLA: Execution-Time Verification with Action-Conditioned World Model for Long-Horizon Mobile Manipulation, 2026 [[paper]](https://arxiv.org/abs/2607.26789) _VLA / robot policy / semantic grounding / action tokens_
- 3DThinkVLA: Endowing Vision-Language-Action Models with Latent 3D Priors via 3D-Thinking-Guided Co-training, 2026 [[paper]](https://scholar.google.com/scholar?q=3DThinkVLA+Endowing+Vision+Language+Action+Models+with+Latent+3D+Priors+via+3D+Thinking+Guided+Co+training) _VLA / robot policy / semantic grounding / action tokens_
- OpenVLA: An Open-Source Vision-Language-Action Model, 2024 [[paper]](https://arxiv.org/abs/2406.09246) _VLA / robot policy / semantic grounding / action tokens_
- Octo: An Open-Source Generalist Robot Policy, 2024 [[paper]](https://arxiv.org/abs/2405.12213) _VLA / robot policy / semantic grounding / action tokens_
- RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control, 2023 [[paper]](https://arxiv.org/abs/2307.15818) _VLA / robot policy / semantic grounding / action tokens_
- PaLM-E: An Embodied Multimodal Language Model, 2023 [[paper]](https://scholar.google.com/scholar?q=PaLM+E+An+Embodied+Multimodal+Language+Model) _VLA / robot policy / semantic grounding / action tokens_
- RoboCat: A Self-Improving Robotic Agent, 2023 [[paper]](https://scholar.google.com/scholar?q=RoboCat+A+Self+Improving+Robotic+Agent) _VLA / robot policy / semantic grounding / action tokens_
- Open X-Embodiment: Robotic Learning Datasets and RT-X Models, 2023 [[paper]](https://arxiv.org/abs/2310.08864) _VLA / robot policy / semantic grounding / action tokens_
- Diffusion Policy: Visuomotor Policy Learning via Action Diffusion, 2023 [[paper]](https://arxiv.org/abs/2303.04137) _VLA / robot policy / semantic grounding / action tokens_
- Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware, 2023 [[paper]](https://scholar.google.com/scholar?q=Learning+Fine+Grained+Bimanual+Manipulation+with+Low+Cost+Hardware) _VLA / robot policy / semantic grounding / action tokens_
- RT-1: Robotics Transformer for Real-World Control at Scale, 2022 [[paper]](https://arxiv.org/abs/2212.06817) _VLA / robot policy / semantic grounding / action tokens_

## Family 1: Latent World Models

_Direction / keywords: latent dynamics / planning / MPC / model-based RL_

- WorldRFT: Latent World Model Planning with Reinforcement Fine-Tuning for Autonomous Driving, 2025 [[paper]](https://arxiv.org/abs/2512.19133) _latent dynamics / planning / MPC / model-based RL_
- TD-MPC2: Scalable, Robust World Models for Continuous Control, 2024 [[paper]](https://arxiv.org/abs/2310.16828) _latent dynamics / planning / MPC / model-based RL_
- Mastering Diverse Domains through World Models, 2023 [[paper]](https://arxiv.org/abs/2301.04104) _latent dynamics / planning / MPC / model-based RL_
- Temporal Difference Learning for Model Predictive Control, 2022 [[paper]](https://scholar.google.com/scholar?q=Temporal+Difference+Learning+for+Model+Predictive+Control) _latent dynamics / planning / MPC / model-based RL_
- Mastering Atari Games with Limited Data, 2021 [[paper]](https://scholar.google.com/scholar?q=Mastering+Atari+Games+with+Limited+Data) _latent dynamics / planning / MPC / model-based RL_
- Mastering Atari with Discrete World Models, 2021 [[paper]](https://scholar.google.com/scholar?q=Mastering+Atari+with+Discrete+World+Models) _latent dynamics / planning / MPC / model-based RL_
- Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model, 2020 [[paper]](https://arxiv.org/abs/1911.08265) _latent dynamics / planning / MPC / model-based RL_
- Dream to Control: Learning Behaviors by Latent Imagination, 2020 [[paper]](https://arxiv.org/abs/1912.01603) _latent dynamics / planning / MPC / model-based RL_
- Stochastic Latent Actor-Critic: Deep Reinforcement Learning with a Latent Variable Model, 2020 [[paper]](https://scholar.google.com/scholar?q=Stochastic+Latent+Actor+Critic+Deep+Reinforcement+Learning+with+a+Latent+Variable+Model) _latent dynamics / planning / MPC / model-based RL_
- Learning Latent Dynamics for Planning from Pixels, 2019 [[paper]](https://arxiv.org/abs/1811.04551) _latent dynamics / planning / MPC / model-based RL_
- When to Trust Your Model: Model-Based Policy Optimization, 2019 [[paper]](https://scholar.google.com/scholar?q=When+to+Trust+Your+Model+Model+Based+Policy+Optimization) _latent dynamics / planning / MPC / model-based RL_
- World Models, 2018 [[paper]](https://arxiv.org/abs/1803.10122) _latent dynamics / planning / MPC / model-based RL_
- Deep Reinforcement Learning in a Handful of Trials using Probabilistic Dynamics Models, 2018 [[paper]](https://scholar.google.com/scholar?q=Deep+Reinforcement+Learning+in+a+Handful+of+Trials+using+Probabilistic+Dynamics+Models) _latent dynamics / planning / MPC / model-based RL_
- Imagination-Augmented Agents for Deep Reinforcement Learning, 2017 [[paper]](https://arxiv.org/abs/1707.06203) _latent dynamics / planning / MPC / model-based RL_
- Embed to Control: A Locally Linear Latent Dynamics Model for Control from Raw Images, 2015 [[paper]](https://scholar.google.com/scholar?q=Embed+to+Control+A+Locally+Linear+Latent+Dynamics+Model+for+Control+from+Raw+Images) _latent dynamics / planning / MPC / model-based RL_

## Family 2: Vision World Models

_Direction / keywords: video world model / controllable generation / interactive simulator_

- minWM: A Full-Stack Open-Source Framework for Real-Time Interactive Video World Models, 2026 [[paper]](https://arxiv.org/abs/2605.30263) _video world model / controllable generation / interactive simulator_
- \$tau\_0\$-WM: A Unified Video-Action World Model for Robotic Manipulation, 2026 [[paper]](https://arxiv.org/abs/2606.01027) _video world model / controllable generation / interactive simulator_
- \$omega\$-EVA: Envision, Verify, and Act with Latent Interactive World Models, 2026 [[paper]](https://arxiv.org/abs/2606.09457) _video world model / controllable generation / interactive simulator_
- YoCausal: How Far is Video Generation from World Model? A Causality Perspective, 2026 [[paper]](https://arxiv.org/abs/2605.30346) _video world model / controllable generation / interactive simulator_
- WorldCraft: From Camera Navigation to Object Manipulation in Interactive Video World Models, 2026 [[paper]](https://arxiv.org/abs/2605.25077) _video world model / controllable generation / interactive simulator_
- What Makes Video World Model Latents Action-Relevant: Prediction over Reconstruction, 2026 [[paper]](https://arxiv.org/abs/2606.07687) _video world model / controllable generation / interactive simulator_
- WBench: A Comprehensive Multi-turn Benchmark for Interactive Video World Model Evaluation, 2026 [[paper]](https://arxiv.org/abs/2605.25874) _video world model / controllable generation / interactive simulator_
- Turning Video Models into Generalist Robot Policies, 2026 [[paper]](https://scholar.google.com/scholar?q=Turning+Video+Models+into+Generalist+Robot+Policies) _video world model / controllable generation / interactive simulator_
- PhyWorld: Physics-Faithful World Model for Video Generation, 2026 [[paper]](https://arxiv.org/abs/2605.19242) _video world model / controllable generation / interactive simulator_
- PanoWorld: Geometry-Consistent Panoramic Video World Modeling, 2026 [[paper]](https://scholar.google.com/scholar?q=PanoWorld+Geometry+Consistent+Panoramic+Video+World+Modeling) _video world model / controllable generation / interactive simulator_
- OptiWorld: Optimal Control for Video World Generation under Physical Constraints, 2026 [[paper]](https://scholar.google.com/scholar?q=OptiWorld+Optimal+Control+for+Video+World+Generation+under+Physical+Constraints) _video world model / controllable generation / interactive simulator_
- Latent Spatial Memory for Video World Models, 2026 [[paper]](https://arxiv.org/abs/2606.09828) _video world model / controllable generation / interactive simulator_
- GEM-4D: Geometry-Enhanced Video World Models for Robot Manipulation, 2026 [[paper]](https://scholar.google.com/scholar?q=GEM+4D+Geometry+Enhanced+Video+World+Models+for+Robot+Manipulation) _video world model / controllable generation / interactive simulator_
- ChronoDreamer: Action-Conditioned World Model as an Online Simulator for Robotic Planning, 2025 [[paper]](https://arxiv.org/abs/2512.18619) _video world model / controllable generation / interactive simulator_
- Memorize-and-Generate: Towards Long-Term Consistency in Real-Time Video Generation, 2025 [[paper]](https://scholar.google.com/scholar?q=Memorize+and+Generate+Towards+Long+Term+Consistency+in+Real+Time+Video+Generation) _video world model / controllable generation / interactive simulator_
- Video Generation Models as World Simulators, 2024 [[paper]](https://openai.com/index/video-generation-models-as-world-simulators/) _video world model / controllable generation / interactive simulator_
- Genie: Generative Interactive Environments, 2024 [[paper]](https://arxiv.org/abs/2402.15391) _video world model / controllable generation / interactive simulator_
- Diffusion Models Are Real-Time Game Engines, 2024 [[paper]](https://arxiv.org/abs/2408.14837) _video world model / controllable generation / interactive simulator_
- VideoPoet: A Large Language Model for Zero-Shot Video Generation, 2023 [[paper]](https://arxiv.org/abs/2312.14125) _video world model / controllable generation / interactive simulator_
- GAIA-1: A Generative World Model for Autonomous Driving, 2023 [[paper]](https://arxiv.org/abs/2309.17080) _video world model / controllable generation / interactive simulator_
- DriveDreamer: Towards Real-world-driven World Models for Autonomous Driving, 2023 [[paper]](https://arxiv.org/abs/2309.09777) _video world model / controllable generation / interactive simulator_
- DrivingDiffusion: Layout-Guided Multi-View Driving Scene Video Generation with Latent Diffusion Model, 2023 [[paper]](https://arxiv.org/abs/2310.07771) _video world model / controllable generation / interactive simulator_
- Learning Interactive Real-World Simulators, 2023 [[paper]](https://arxiv.org/abs/2310.06114) _video world model / controllable generation / interactive simulator_
- Phenaki: Variable Length Video Generation from Open Domain Textual Descriptions, 2022 [[paper]](https://arxiv.org/abs/2210.02399) _video world model / controllable generation / interactive simulator_
- Imagen Video: High Definition Video Generation with Diffusion Models, 2022 [[paper]](https://arxiv.org/abs/2210.02303) _video world model / controllable generation / interactive simulator_
- VideoGPT: Video Generation using VQ-VAE and Transformers, 2021 [[paper]](https://arxiv.org/abs/2104.10157) _video world model / controllable generation / interactive simulator_
- Learning to Simulate Dynamic Environments with GameGAN, 2020 [[paper]](https://arxiv.org/abs/2005.12126) _video world model / controllable generation / interactive simulator_
- Visual Foresight: Model-Based Deep Reinforcement Learning for Vision-Based Robotic Control, 2018 [[paper]](https://arxiv.org/abs/1812.00568) _video world model / controllable generation / interactive simulator_
- Action-Conditional Video Prediction using Deep Networks in Atari Games, 2015 [[paper]](https://arxiv.org/abs/1507.08750) _video world model / controllable generation / interactive simulator_

## Family 3: World Action Models

_Direction / keywords: WAM / joint visual-action generation / executable futures_

- WorldVLN: Autoregressive World Action Model for Aerial Vision-Language Navigation, 2026 [[paper]](https://scholar.google.com/scholar?q=WorldVLN+Autoregressive+World+Action+Model+for+Aerial+Vision+Language+Navigation) _WAM / joint visual-action generation / executable futures_
- WorldDiT: A Unified Diffusion Architecture for World and Action Modeling, 2026 [[paper]](https://arxiv.org/abs/2607.23909) _WAM / joint visual-action generation / executable futures_
- T-TWAM: Scaling Tactile-Native World-Action Model for Contact-Rich Manipulation, 2026 [[paper]](https://arxiv.org/abs/2607.23783) _WAM / joint visual-action generation / executable futures_
- Qwen-RobotWorld: Unifying Embodied World Modeling through Language-Conditioned Video Generation, 2026 [[paper]](https://arxiv.org/abs/2606.17030) _WAM / joint visual-action generation / executable futures_
- PAVXploreRL: Physical-Action-Visual World Model Reinforcement Learning with Action Exploration, 2026 [[paper]](https://arxiv.org/abs/2607.16602) _WAM / joint visual-action generation / executable futures_
- OSCAR: Omni-Embodiment Skeleton-Conditioned World Action Model for Robotics, 2026 [[paper]](https://scholar.google.com/scholar?q=OSCAR+Omni+Embodiment+Skeleton+Conditioned+World+Action+Model+for+Robotics) _WAM / joint visual-action generation / executable futures_
- NVIDIA OmniDreams: Real-Time Generative World Model for Closed-Loop Autonomous Vehicle Simulation, 2026 [[paper]](https://arxiv.org/abs/2606.03159) _WAM / joint visual-action generation / executable futures_
- MotionWAM: Towards Foundation World Action Models for Real-Time Humanoid Loco-Manipulation, 2026 [[paper]](https://arxiv.org/abs/2606.09215) _WAM / joint visual-action generation / executable futures_
- Masked Visual Actions for Unified World Modeling, 2026 [[paper]](https://arxiv.org/abs/2607.19343) _WAM / joint visual-action generation / executable futures_
- ImagineUAV: Aerial Vision-Language Navigation via World-Action Modeling and Kinodynamic Planning, 2026 [[paper]](https://scholar.google.com/scholar?q=ImagineUAV+Aerial+Vision+Language+Navigation+via+World+Action+Modeling+and+Kinodynamic+Planning) _WAM / joint visual-action generation / executable futures_
- HarmoWAM: Harmonizing Generalizable and Precise Manipulation via Adaptive World Action Models, 2026 [[paper]](https://arxiv.org/abs/2605.10942) _WAM / joint visual-action generation / executable futures_
- GeoWorldAD: Geometry World Action Model for Autonomous Driving, 2026 [[paper]](https://arxiv.org/abs/2607.17521) _WAM / joint visual-action generation / executable futures_
- GeoSem-WAM: Geometry- and Semantic-Aware World Action Models, 2026 [[paper]](https://arxiv.org/abs/2606.03188) _WAM / joint visual-action generation / executable futures_
- DriftWorld: Fast World Modeling through Drifting, 2026 [[paper]](https://arxiv.org/abs/2607.15065) _WAM / joint visual-action generation / executable futures_
- Dream-Tac: A Unified Tactile World Action Model for Contact-Rich Robot Manipulation, 2026 [[paper]](https://arxiv.org/abs/2606.08737) _WAM / joint visual-action generation / executable futures_
- Discrete-WAM: Unified Discrete Vision-Action Token Editing for World-Policy Learning, 2026 [[paper]](https://arxiv.org/abs/2606.05645) _WAM / joint visual-action generation / executable futures_
- DeVA: Decoupled Video-Action Model with Physical Guidance for Robot Policy Learning, 2026 [[paper]](https://arxiv.org/abs/2607.24159) _WAM / joint visual-action generation / executable futures_
- Cosmos 3: Omnimodal World Models for Physical AI, 2026 [[paper]](https://arxiv.org/abs/2606.02800) _WAM / joint visual-action generation / executable futures_
- CLAW: Learning Continuous Latent Action World Models via Adversarial Latent Regularization, 2026 [[paper]](https://arxiv.org/abs/2606.04130) _WAM / joint visual-action generation / executable futures_
- BadWAM: When World-Action Models Dream Right but Act Wrong, 2026 [[paper]](https://arxiv.org/abs/2607.15207) _WAM / joint visual-action generation / executable futures_
- AeroAct: Action-Centered World-Action Models for Language-Conditioned Quadrotor Flight, 2026 [[paper]](https://arxiv.org/abs/2607.14997) _WAM / joint visual-action generation / executable futures_

## Autonomous Driving and 3D/BEV World Models

_Direction / keywords: driving / BEV / occupancy / closed-loop simulation_

- Xiaomi Auto World Model: A Joint World Model Integrating Reconstruction and Generation for Autonomous Driving, 2026 [[paper]](https://scholar.google.com/scholar?q=Xiaomi+Auto+World+Model+A+Joint+World+Model+Integrating+Reconstruction+and+Generation+for+Autonomous+Driving) _driving / BEV / occupancy / closed-loop simulation_
- Unified Driving Tokens: Representation- and Geometry-Guided Discrete Tokenizer for Driving World Models and Planning, 2026 [[paper]](https://scholar.google.com/scholar?q=Unified+Driving+Tokens+Representation+and+Geometry+Guided+Discrete+Tokenizer+for+Driving+World+Models+and+Planning) _driving / BEV / occupancy / closed-loop simulation_
- Think at 5 Hz, Act at 20 Hz: Asynchronous Fast-Slow Vision-Language-Action Inference for Closed-Loop Driving, 2026 [[paper]](https://arxiv.org/abs/2607.15621) _driving / BEV / occupancy / closed-loop simulation_
- SparseWorld: Enhancing End-to-End Autonomous Driving via World Models with Sparse Scene Representation, 2026 [[paper]](https://arxiv.org/abs/2605.24354) _driving / BEV / occupancy / closed-loop simulation_
- Reason--Imagine--Act: Closed-Loop LLM Decision Making with World Models for Autonomous Driving, 2026 [[paper]](https://arxiv.org/abs/2605.24004) _driving / BEV / occupancy / closed-loop simulation_
- PLAN-S: Bridging Planning with Latent Style Dynamics for Autonomous Driving World Models, 2026 [[paper]](https://arxiv.org/abs/2606.06014) _driving / BEV / occupancy / closed-loop simulation_
- HorizonDrive: Self-Corrective Autoregressive World Model for Long-horizon Driving Simulation, 2026 [[paper]](https://scholar.google.com/scholar?q=HorizonDrive+Self+Corrective+Autoregressive+World+Model+for+Long+horizon+Driving+Simulation) _driving / BEV / occupancy / closed-loop simulation_
- HEAT: Heterogeneous End-to-End Autonomous Driving via Trajectory-Guided World Models, 2026 [[paper]](https://arxiv.org/abs/2605.19631) _driving / BEV / occupancy / closed-loop simulation_
- DriveMA: Driving Vision-Language-Action Models with Verifiable Meta-Actions, 2026 [[paper]](https://scholar.google.com/scholar?q=DriveMA+Driving+Vision+Language+Action+Models+with+Verifiable+Meta+Actions) _driving / BEV / occupancy / closed-loop simulation_
- Beyond Euclidean Proximity: Repairing Latent World Models with Horizon-Matched Trajectory Reachability Metrics, 2026 [[paper]](https://arxiv.org/abs/2605.22164) _driving / BEV / occupancy / closed-loop simulation_
- OccSTeP: Benchmarking 4D Occupancy Spatio-Temporal Persistence, 2025 [[paper]](https://scholar.google.com/scholar?q=OccSTeP+Benchmarking+4D+Occupancy+Spatio+Temporal+Persistence) _driving / BEV / occupancy / closed-loop simulation_
- InDRiVE: Reward-Free World-Model Pretraining for Autonomous Driving via Latent Disagreement, 2025 [[paper]](https://scholar.google.com/scholar?q=InDRiVE+Reward+Free+World+Model+Pretraining+for+Autonomous+Driving+via+Latent+Disagreement) _driving / BEV / occupancy / closed-loop simulation_
- VAD: Vectorized Scene Representation for Efficient Autonomous Driving, 2023 [[paper]](https://arxiv.org/abs/2303.12077) _driving / BEV / occupancy / closed-loop simulation_
- SurroundOcc: Multi-Camera 3D Occupancy Prediction for Autonomous Driving, 2023 [[paper]](https://arxiv.org/abs/2303.09551) _driving / BEV / occupancy / closed-loop simulation_
- Planning-oriented Autonomous Driving, 2023 [[paper]](https://arxiv.org/abs/2212.10156) _driving / BEV / occupancy / closed-loop simulation_
- OccFormer: Dual-path Transformer for Vision-based 3D Semantic Occupancy Prediction, 2023 [[paper]](https://arxiv.org/abs/2304.05316) _driving / BEV / occupancy / closed-loop simulation_
- BEVFormer: Learning Bird's-Eye-View Representation from Multi-Camera Images via Spatiotemporal Transformers, 2022 [[paper]](https://arxiv.org/abs/2203.17270) _driving / BEV / occupancy / closed-loop simulation_

## Digital Agents and Verification

_Direction / keywords: web / OS / tool-use / execution-time verification_

- WMAttack: Automated Attack Search for Adversarial Evaluation of World-Model Agents, 2026 [[paper]](https://arxiv.org/abs/2605.23220) _web / OS / tool-use / execution-time verification_
- Policy and World Modeling Co-Training for Language Agents, 2026 [[paper]](https://arxiv.org/abs/2606.02388) _web / OS / tool-use / execution-time verification_
- MIRAGE: Mobile Agents with Implicit Reasoning and Generative World Models, 2026 [[paper]](https://scholar.google.com/scholar?q=MIRAGE+Mobile+Agents+with+Implicit+Reasoning+and+Generative+World+Models) _web / OS / tool-use / execution-time verification_
- Web World Models, 2025 [[paper]](https://scholar.google.com/scholar?q=Web+World+Models) _web / OS / tool-use / execution-time verification_
- OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments, 2024 [[paper]](https://arxiv.org/abs/2404.07972) _web / OS / tool-use / execution-time verification_
- ToolEmu: Identifying the Risks of LM Agents with an LM-Emulated Sandbox, 2023 [[paper]](https://arxiv.org/abs/2309.15817) _web / OS / tool-use / execution-time verification_
- WebArena: A Realistic Web Environment for Building Autonomous Agents, 2023 [[paper]](https://arxiv.org/abs/2307.13854) _web / OS / tool-use / execution-time verification_
- Mind2Web: Towards a Generalist Agent for the Web, 2023 [[paper]](https://scholar.google.com/scholar?q=Mind2Web+Towards+a+Generalist+Agent+for+the+Web) _web / OS / tool-use / execution-time verification_
- SWE-bench: Can Language Models Resolve Real-World GitHub Issues?, 2023 [[paper]](https://arxiv.org/abs/2310.06770) _web / OS / tool-use / execution-time verification_
- World of Bits: An Open-Domain Platform for Web-Based Agents, 2017 [[paper]](https://scholar.google.com/scholar?q=World+of+Bits+An+Open+Domain+Platform+for+Web+Based+Agents) _web / OS / tool-use / execution-time verification_

## Maintenance Notes

- Current README count: 115 papers/resources.
- Primary metadata source: [../references.bib](../references.bib).
- Current survey source: [../survey-v1.tex](../survey-v1.tex).
- Current PDF: [../build/world-model-survey-v1.pdf](../build/world-model-survey-v1.pdf).
- Legacy four-paradigm seed table: [papers-by-paradigm.md](papers-by-paradigm.md).
- To add or remove papers, update `SECTIONS` in [../tools/build_awesome_readme.py](../tools/build_awesome_readme.py), then run `python3 tools/build_awesome_readme.py`.
- Before camera-ready use, replace Scholar fallback links with DOI, arXiv, OpenReview, project pages, or official venue URLs where available.
