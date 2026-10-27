# 李羽韬 · Yutao Li

**应用机器学习 · AI Agent · 计算机视觉与机器人感知**

[English](./README.md) · [中文介绍](./README.zh-CN.md) · [作品集与演示](./portfolio/README.md)

目前在**加州大学圣迭戈分校（UC San Diego）**攻读电子与计算机工程硕士，计算机工程方向；本科毕业于**香港中文大学（深圳）**电子信息工程专业。

我的经历涵盖AI应用开发、机器人感知，以及神经网络建模与遥感图像分割研究，关注算法实现、实验评估和系统可靠性。正在寻找中国或美国的机器学习、AI应用及机器人感知相关全职机会。

[英文简历（PDF）](https://github.com/Forge-Lee/Forge-Lee/blob/main/Yutao_Li_2027_Resume_general_1.pdf) · [LinkedIn](https://www.linkedin.com/in/yutao-li-forge1813/) · [Google Scholar](https://scholar.google.com/citations?user=koWNqn4AAAAJ) · [邮箱](mailto:yul389@ucsd.edu)

## 作品集导航

| 材料 | 直接访问 |
| --- | --- |
| Job Agent | [代码](https://github.com/Forge-Lee/job_agent) · [演示视频](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view) · [匹配报告示例](https://github.com/Forge-Lee/job_agent/blob/main/outputs/sample/match_report.md) |
| RGB-D语义建图 | [代码](https://github.com/Forge-Lee/rgbd-semantic-mapping) · [演示视频](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) |
| 视觉—惯性SLAM | [项目介绍](./portfolio/README.md#3-visual-inertial-slam) |
| NeRA | [第一作者论文](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803) |
| EDAgent | [项目介绍](./portfolio/README.md#5-edagent-llm-agents-for-economic-dispatch) |

[英文作品集导览](./portfolio/README.md)说明各项目内容、个人贡献与建议关注点；部分原始材料保留中文。

## 代表开发项目

### Job Agent：AI求职助手

**个人独立项目 · 2026.06—2026.08**  
Python · ReAct · RAG · ChromaDB · Pydantic · Streamlit · Docker

面向岗位信息整理、经历匹配与申请材料生成，开发可持续保存申请记录的LLM应用，串联简历解析、职位分析、匹配评估、材料生成和申请管理。

- 独立完成系统设计、开发与集成，结合规则匹配和LLM语义分析展示相关经历、能力缺口与匹配依据。
- 实现ReAct多步工具调用及可查看的执行轨迹，支持关键词、Embedding及Chroma向量检索，复用历史申请信息。
- 加入结构化输出校验、JSON／Markdown状态持久化和可配置LLM客户端，提供CLI与Streamlit交互界面，并支持Docker运行。

[代码与项目说明](https://github.com/Forge-Lee/job_agent) · [匹配报告示例](https://github.com/Forge-Lee/job_agent/blob/main/outputs/sample/match_report.md) · [演示视频](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view)

<a href="https://raw.githubusercontent.com/Forge-Lee/job_agent/main/docs/assets/job_analysis.png"><img src="https://raw.githubusercontent.com/Forge-Lee/job_agent/main/docs/assets/job_analysis.png" alt="Job Agent岗位分析示例界面" width="760"></a>

*界面使用示例岗位与候选人数据；页面中的匹配分数属于应用输出，不代表系统评测指标。*

### 可回放RGB-D语义建图系统

**个人独立项目 · 2026.07—2026.08**  
Python · C++17 · ROS 2 · PyTorch · SegFormer · RGB-D

基于记录的RGB-D观测与数据集提供的相机位姿，构建逐帧更新的三维语义体素地图，完成从二维语义感知到三维投影、融合与可视化的处理流程。

- 实现RGB-D与位姿数据关联、SegFormer语义分割、深度反投影、坐标变换及置信度加权语义融合。
- 将Python感知节点与C++17建图后端集成为ROS 2系统，同步处理多路消息，通过PointCloud2与RViz2展示地图。
- 在**80帧、约116万次观测**上验证Python／C++结果一致性；核心建图模块基准测试中，中位耗时由**5.526秒降至2.997秒，实现1.84×加速**。该指标衡量建图模块，不是包含语义分割的端到端性能。

[代码与项目说明](https://github.com/Forge-Lee/rgbd-semantic-mapping) · [增量建图视频](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) · [结果展示](https://github.com/Forge-Lee/rgbd-semantic-mapping#example-results)

<a href="https://raw.githubusercontent.com/Forge-Lee/rgbd-semantic-mapping/main/assets/ros2_semantic_map.png"><img src="https://raw.githubusercontent.com/Forge-Lee/rgbd-semantic-mapping/main/assets/ros2_semantic_map.png" alt="ROS 2 RViz2中的RGB-D语义体素地图" width="760"></a>

## 科研经历

### NeRA：基于神经反射与衰减场的无线电地图重建

**科研助理／论文第一作者 · 2022.07—2024.05**  
香港中文大学（深圳）· 黄川教授指导

通过神经反射场与衰减场学习真实环境结构对无线信号传播的影响，实现无线电地图重建。本人工作涉及真实环境数据采集与预处理、PyTorch模型实现和训练、实验评估、结果分析及论文撰写。

- 在论文报告的有限数据实验中，使用**20%的实测数据**训练，相比NeRF²基线，平均绝对预测误差降低**26%**。
- 相关成果以第一作者发表于**IEEE VTC 2024-Fall**。

**Yutao Li**, Yancheng Wang, Chuan Huang. “NeRA: Neural Reflectance and Attenuation Fields for Radio Map Reconstruction.” [论文／DOI](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803)。

### 基于LoRA微调SAM的多模态遥感语义分割

**科研助理 · 2024.09—2024.12**  
香港中文大学（深圳）· 潘文安教授指导

研究SAM在遥感语义分割任务中的参数高效适配，在不同网络层引入不同Rank的LoRA模块，并结合多模态特征融合。本人工作包括模型与融合模块实现、数据预处理、PyTorch训练与评估，以及不同输入组合和适配器配置的对比实验。

## 课程项目

### EDAgent：面向电力经济调度的LLM Agent

**UC San Diego课程团队项目 · 2026.01—2026.03**  
ReAct · CVXPY · OSQP · FastAPI · Streamlit

团队基于ReAct构建可调用领域工具的智能体，将自然语言调度请求转化为IEEE 14／30／57／118节点系统上的约束优化求解。

**个人贡献：**基线方法复现、对比实验、实验评估与结果分析。

[项目介绍与个人贡献](./portfolio/README.md#5-edagent-llm-agents-for-economic-dispatch)

### 视觉—惯性SLAM

**UC San Diego课程项目 · 2026.02—2026.03**  
Python · NumPy · SciPy · OpenCV · EKF · SE(3)

实现基于SE(3)的IMU运动预测、协方差传播、双目地标初始化及EKF测量更新，联合估计机器人位姿与三维地标。在两组MIT Clearpath Jackal序列上完成轨迹和地图可视化，并分析视觉观测对IMU累积漂移的校正作用。

[项目介绍](./portfolio/README.md#3-visual-inertial-slam)

## 教育背景与技术工具

- **加州大学圣迭戈分校**：电子与计算机工程硕士，计算机工程方向；2025.09入学，预计2026.12毕业。
- **香港中文大学（深圳）**：电子信息工程工学学士；2021.09—2025.07。

**开发基础：**熟悉Python、PyTorch；具有C++17、Linux、Docker与Git实践经验。  
**AI应用：**LLM API、ReAct、RAG、ChromaDB、Pydantic、FastAPI、Streamlit。  
**视觉与机器人：**OpenCV、ROS 2、RGB-D几何、语义分割、体素建图及基于EKF的状态估计。

更多论文见[Google Scholar](https://scholar.google.com/citations?user=koWNqn4AAAAJ)。项目介绍与公开演示见[作品集导览](./portfolio/README.md)；项目报告及其他研究材料可通过[yul389@ucsd.edu](mailto:yul389@ucsd.edu)联系。