<p align="center">
  <img src="https://raw.githubusercontent.com/CyanStarNight/CloudNativeSim/master/docs/assets/logo.png" alt="CloudNativeSim Logo" width=30%>
</p>
<p align="center">
| <a href="https://docs.cloudnativesim"><b>Documentation</b></a> | <a href=""><b>Paper</b></a> | <a href="https://github.com/CyanStarNight/CloudNativeSim/issues"><b>Issues</b></a>  |  <a href="https://github.com/users/CyanStarNight/projects/1"><b>Schedule</b></a> |
</p>

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
Special thanks to @beyondHJM for assisting with the design and configuration of the Grafana panels.

## Citation
