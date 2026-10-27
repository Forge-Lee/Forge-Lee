# Yutao Li — Project Portfolio

[GitHub profile](https://github.com/Forge-Lee) · [English introduction](../README.md) · [中文介绍](../README.zh-CN.md) · [Resume (PDF)](../Yutao_Li_2027_Resume_general_1.pdf)

Selected work in **AI agents, computer vision, and robotics perception**. This guide brings together public demos, source repositories, a published research paper, and English summaries of my contributions. Some demo content is in Chinese. Course project reports are available on request.

## Quick Access

| Work sample | Materials | My contribution |
| --- | --- | --- |
| **Job Agent** | [Demo video](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view) · [Code](https://github.com/Forge-Lee/job_agent) · [Example output](https://github.com/Forge-Lee/job_agent/blob/main/outputs/sample/match_report.md) | Independent design, development, and integration |
| **RGB-D Semantic Mapping** | [Demo video](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) · [Code](https://github.com/Forge-Lee/rgbd-semantic-mapping) | Independent perception and mapping pipeline; C++17 refactoring |
| **Visual-Inertial SLAM** | [Project summary](#3-visual-inertial-slam) | EKF state estimation, stereo geometry, mapping, and evaluation |
| **NeRA** | [Published paper](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803) | Model implementation, real data collection, training, evaluation, and writing |
| **EDAgent** | [Project summary](#5-edagent-llm-agents-for-economic-dispatch) | Baseline reproduction and comparative experimental evaluation |

## 1. Job Agent: Agentic AI Job Application Assistant

**Independent project · Python, ReAct, RAG, ChromaDB, Pydantic, Streamlit, Docker**

Developed a complete application covering job description parsing, candidate–job matching, tailored application material generation, and application tracking. A ReAct workflow coordinates tool calls and observations; retrieval from historical records provides context, while schema validation and persistent state support reliable application behavior.

**What to look for:** multi-step tool use, retrieval and application memory, inspectable execution traces, and integration into a usable interface.

[Watch the full demo](https://drive.google.com/file/d/1esUKIsCuKqV9EU48AhRSLyjlZVBMsb3Y/view) · [Source and setup](https://github.com/Forge-Lee/job_agent) · [Workflow design](https://github.com/Forge-Lee/job_agent/blob/main/docs/workflow_design.md)

<a href="https://github.com/Forge-Lee/job_agent#demo"><img src="https://raw.githubusercontent.com/Forge-Lee/job_agent/main/docs/assets/react_agent_trace.png" alt="Job Agent ReAct trace with tool calls and observations" width="760"></a>

*Screenshots use example inputs. Candidate match scores are application outputs rather than benchmark performance.*

## 2. Replayable RGB-D Semantic Mapping

**Independent project · Python, C++17, ROS 2, PyTorch, SegFormer**

Built an incremental 3D semantic voxel map from RGB-D observations and dataset-provided camera poses. The pipeline combines synchronization, semantic segmentation, depth back-projection, coordinate transforms, and confidence-weighted fusion. ROS 2 nodes publish the fused map as PointCloud2 for RViz2 visualization.

Refactored the core fusion module from Python to C++17 and verified consistency over **80 frames and approximately 1.16 million observations**. Median runtime fell from **5.526 s to 2.997 s**, a **1.84× speedup**. This benchmark measures the core mapping module and excludes semantic segmentation.

**What to look for:** geometry and semantic fusion, incremental updates, robotics middleware integration, and optimization with cross-language verification.

[Watch the incremental mapping demo](https://github.com/Forge-Lee/rgbd-semantic-mapping/blob/main/assets/incremental_mapping_demo.mp4) · [Source and setup](https://github.com/Forge-Lee/rgbd-semantic-mapping)

<a href="https://github.com/Forge-Lee/rgbd-semantic-mapping#example-results"><img src="https://raw.githubusercontent.com/Forge-Lee/rgbd-semantic-mapping/main/assets/final_semantic_map.png" alt="Final fused 3D semantic map from RGB-D observations" width="760"></a>

## 3. Visual-Inertial SLAM

**Course project · Python, NumPy, SciPy, OpenCV, EKF, SE(3)**

Implemented an EKF-based system combining IMU measurements and stereo observations to jointly estimate six-degree-of-freedom robot poses and 3D landmarks. The work includes motion prediction on SE(3), Jacobians and covariance propagation, stereo landmark initialization, and visual measurement updates.

**What to look for:** mathematical formulation, sensor fusion, trajectory and landmark visualizations, and correction of accumulated IMU drift.

Project report available on request: [email me](mailto:yul389@ucsd.edu).

## 4. NeRA: Neural Reflectance and Attenuation Fields for Radio Map Reconstruction

**Research assistant / first author · PyTorch · IEEE VTC 2024-Fall**

Modeled how real environmental structure affects radio propagation using learnable reflectance and attenuation fields. My work included real-world data collection and preprocessing, model implementation and training, experimental analysis, and manuscript preparation.

The paper reports a **26% reduction in mean absolute prediction error compared with NeRF² when trained on 20% of measured data**.

**What to look for:** neural-field modeling, integration of environmental geometry and propagation structure, real-world experiments, and quantitative comparison.

[Read the published paper](https://doi.org/10.1109/VTC2024-Fall63153.2024.10757803)

## 5. EDAgent: LLM Agents for Economic Dispatch

**Course team project · ReAct, CVXPY, OSQP, FastAPI, Streamlit**

The team developed a tool-augmented LLM framework that translates natural-language economic dispatch requests into constrained optimization problems, executes domain tools, and evaluates the resulting solutions.

**My contribution:** reproducing baseline methods, configuring economic dispatch experiments, comparing task success and constraint satisfaction, and analyzing cost error. The report describes the full team's framework and results.

**What to look for:** task-specific tool integration, evaluation design, baseline comparisons, and the relationship between language-model outputs and numerical constraints.

Team project report available on request: [email me](mailto:yul389@ucsd.edu).

---

Contact: [yul389@ucsd.edu](mailto:yul389@ucsd.edu) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=koWNqn4AAAAJ)
