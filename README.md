<p align="center">
  <img src="https://raw.githubusercontent.com/CyanStarNight/CloudNativeSim/master/docs/assets/logo.png" alt="CloudNativeSim Logo" width=30%>
</p>

<div align="center">
  
[![GPL licensed](https://img.shields.io/badge/license-GPL-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
[![Progress Tracker](https://img.shields.io/badge/Progess-track-green)](https://github.com/users/CyanStarNight/projects/1)
[![arXiv](https://img.shields.io/badge/arXiv-2409.05093-b31b1b.svg)](https://arxiv.org/abs/2409.05093)
![version](https://img.shields.io/badge/version-1.0-blue)
[![GitHub Repo stars](https://img.shields.io/github/stars/CyanStarNight/CloudNativeSim)](https://github.com/CyanStarNight/CloudNativeSim)

</div>

## About

CloudNativeSim is a toolkit for modeling and simulation of cloud-native applications. It employs a multi-layered architecture, allowing for high extensibility and customization. Below is an overview of the CloudNativeSim architecture:
<p align="center">
  <img src="https://raw.githubusercontent.com/CyanStarNight/CloudNativeSim/master/docs/assets/Architecture.png" alt="Architecture" width=60%>
</p>

Through detailed modeling of cloud-native environments and microservices architecture, CloudNativeSim provides these key features:
+ Comprehensive modeling approach
+ High extensibility and customization
+ Simulation of dynamic request generation and dispatching
+ Innovative cloudlet scheduling mechanism
+ Latency calculation based on the critical path
+ QoS metrics feedback
+ New policy interfaces
+ Grafana Dashboard Visualization

If you’re using this simulator, please ★Star this repository to show your interest!

## Getting Started
1. Clone the CloudNativeSim Git repository to local folder:
    ```shell
    git clone https://github.com/CyanStarNight/CloudNativeSim.git
    ```
2. Verify the development environment: Ensure that Java version 17 or higher is installed, the CloudSim 3.0 JAR package is available, and all Maven dependencies are fully imported.
3. Run the example files (e.g., `SockShopExample.java`) to get started


## Visualization
CloudNativeSim allows users to export simulation results to files and visualize them in Grafana. Follow these steps:
1. Import the panel styles from the `visualization/styles` folder into Grafana.
2. Add fields in the main CloudNativeSim run file to enable data export to files, such as:
   ```java
   Reporter.writeResourceUsage("path/xxx");
   Reporter.writeStatisticsToCsv(apis, "path/xxx");
   ```
3. If you need to observe service dependencies in Grafana, ensure that the service registration files comply with the [NodeGraph](https://docs.aws.amazon.com/grafana/latest/userguide/v9-panels-node-graph.html) requirements.

The visualization results are shown below:

<p align="center">
  <img src="https://raw.githubusercontent.com/CyanStarNight/CloudNativeSim/master/docs/assets/QPS grafana.png" alt="QPS Visualization" width=60%>
  <img src="https://raw.githubusercontent.com/CyanStarNight/CloudNativeSim/master/docs/assets/service dependency.png" alt="Service Dependency Visualization" width=35%>
</p>


## Contributing and Acknowledgement

We welcome your contributions to the project! Please read the [CONTRIBUTING.md](./CONTRIBUTING.md)  before you start. The guide includes information on various ways to contribute, such as requesting features, reporting issues, fixing bugs, or adding new features.
Special thanks to [@beyondHJM](https://github.com/beyondHJM) for assisting with the design and configuration of the Grafana panels.

## Paper
You can refer to our paper published on [arxiv](https://arxiv.org/abs/2409.05093) or [whiley](https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.3417).
```latex
@article{wu2024cloudnativesim,
  title={Cloudnativesim: A Toolkit for Modeling and Simulation of Cloud-Native Applications},
  author={Wu, Jingfeng and Xu, Minxian and He, Yiyuan and Ye, Kejiang and Xu, Chengzhong},
  journal={Software: Practice and experience},
  year={2025},
  doi={10.1002/spe.3417}
}
```
