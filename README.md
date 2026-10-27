<!--## Hi there 👋-->

<!--
**Forge-Lee/Forge-Lee** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# Hi there 👋, I'm Yutao Li

M.S. ECE student at UC San Diego, focusing on Machine Learning, Computer Vision, Robotics, and LLM-based AI systems.

[Project Portfolio](./portfolio/README.md) · [中文介绍](./README.zh-CN.md) · [Resume (PDF)](./Yutao_Li_2027_Resume_general_1.pdf)

## Portfolio at a Glance

| Work sample | Focus | Explore |
| --- | --- | --- |
| **Job Agent** | ReAct tool use, RAG, structured outputs, application memory | [Code](https://github.com/Forge-Lee/job_agent) · [Video](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view) · [Sample report](https://github.com/Forge-Lee/job_agent/blob/main/outputs/sample/match_report.md) |
| **RGB-D Semantic Mapping** | 3D perception, ROS 2, semantic voxel fusion, C++17 | [Code](https://github.com/Forge-Lee/rgbd-semantic-mapping) · [Video](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) |
| **Visual-Inertial SLAM** | Stereo vision, EKF, SE(3), sensor fusion | [Project summary](./portfolio/README.md#3-visual-inertial-slam) |
| **NeRA** | Neural fields for radio map reconstruction; first-author IEEE VTC paper | [Published paper](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803) |
| **EDAgent** | LLM agents for constrained economic dispatch; team project | [Project summary](./portfolio/README.md#5-edagent-llm-agents-for-economic-dispatch) |

The [portfolio guide](./portfolio/README.md) brings together project summaries, individual contributions, public code, demos, and the published paper. Some demo content is in Chinese.

## Interests
- Applied AI / LLM Agents / RAG
- Computer Vision and Robotics Perception
- ML Systems and AI Infrastructure

## Featured Projects
### AI Job Application Assistant Agent
LLM-based workflow that parses job descriptions, matches candidate profiles, generates application materials, validates outputs, and tracks applications.

**Independent project · Python, ReAct, ChromaDB, Pydantic, Streamlit, Docker**

- Implemented multi-step tool calls, retrieval from past applications, structured output validation, and persistent application state.
- Integrated CLI and Streamlit interfaces with a configurable LLM client and Docker support.

[Source & setup](https://github.com/Forge-Lee/job_agent) · [Watch demo](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view) · [Workflow design](https://github.com/Forge-Lee/job_agent/blob/main/docs/workflow_design.md)

<a href="https://github.com/Forge-Lee/job_agent#demo"><img src="https://raw.githubusercontent.com/Forge-Lee/job_agent/main/docs/assets/job_analysis.png" alt="Job Agent interface showing job analysis and candidate matching" width="760"></a>

*The interface uses sample inputs. Displayed match scores are application outputs, not system evaluation metrics.*

### RGB-D Semantic Mapping
Robotics perception project involving RGB-D synchronization, pose matching, 3D projection, and semantic map construction.

**Independent project · Python, C++17, ROS 2, PyTorch, SegFormer**

- Built incremental semantic voxel maps from recorded RGB-D observations using dataset-provided camera poses.
- Integrated replay, segmentation, and mapping through ROS 2, publishing PointCloud2 maps for RViz2 visualization.
- Validated Python/C++ consistency on **80 frames and approximately 1.16 million observations**. Refactoring the core fusion module reduced median runtime from **5.526 s to 2.997 s (1.84× speedup)**; this benchmark excludes semantic segmentation.

[Source & setup](https://github.com/Forge-Lee/rgbd-semantic-mapping) · [Watch demo](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) · [Results](https://github.com/Forge-Lee/rgbd-semantic-mapping#example-results)

<a href="https://github.com/Forge-Lee/rgbd-semantic-mapping#example-results"><img src="https://raw.githubusercontent.com/Forge-Lee/rgbd-semantic-mapping/main/assets/ros2_semantic_map.png" alt="RGB-D semantic voxel map visualized in ROS 2 RViz2" width="760"></a>

### EdAgent
ReAct-style LLM agent for economic dispatch with domain tools, optimization backend, and Streamlit/FastAPI interfaces.

**Course team project · ReAct, CVXPY, OSQP, FastAPI, Streamlit**

My contributions focused on **baseline reproduction, experiment configuration, comparative evaluation, and result analysis**.

[Project summary and contributions](./portfolio/README.md#5-edagent-llm-agents-for-economic-dispatch)

### Visual-Inertial SLAM

**Course project · Python, NumPy, SciPy, OpenCV, EKF, SE(3)**

Implemented joint estimation of robot poses and 3D landmarks from IMU measurements and stereo observations, including motion prediction, covariance propagation, and visual measurement updates. Evaluated trajectories and landmark maps on MIT Clearpath Jackal sequences.

[Project summary](./portfolio/README.md#3-visual-inertial-slam)

### Multimodal Remote Sensing Segmentation with LoRA-SAM

**Research assistant · PyTorch, SAM, LoRA, multimodal feature fusion**

Implemented multimodal fusion and parameter-efficient adaptation of SAM for remote sensing segmentation, including data preprocessing, training, evaluation, and comparisons across input modalities and LoRA configurations.

## Publications
- NeRA: Neural Reflectance and Attenuation Fields for Radio Map Reconstruction, IEEE VTC 2024

First author of **NeRA: Neural Reflectance and Attenuation Fields for Radio Map Reconstruction**. My work covered model implementation and training, real-world data collection, experimental evaluation, and manuscript preparation. The paper reports a **26% reduction in mean absolute error over NeRF² when trained on 20% of measured data**.

[Read the published paper](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=koWNqn4AAAAJ)

## Education

- **UC San Diego** — M.S. in Electrical and Computer Engineering, Computer Engineering track; expected December 2026.
- **The Chinese University of Hong Kong, Shenzhen** — B.Eng. in Electronic Information Engineering, 2025.

## Links
- Resume: [PDF](./Yutao_Li_2027_Resume_general_1.pdf)
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/yutao-li-forge1813/)
- Google Scholar: [Google Scholar](https://scholar.google.com/citations?hl=en&user=koWNqn4AAAAJ)
- Email: [yul389@ucsd.edu](mailto:yul389@ucsd.edu)
