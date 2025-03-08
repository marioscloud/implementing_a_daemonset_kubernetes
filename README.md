This repository contains the resources for a hands-on lab from the course Introduction to Containers with Docker, Kubernetes & OpenShift, part of the IBM DevOps and Software Engineering Professional Certificate. The lab demonstrates how to implement a DaemonSet in Kubernetes. 

A DaemonSet ensures that a copy of a specific Pod runs on all (or some) nodes in the cluster. It is particularly useful for deploying system-level applications that provide essential services across the nodes in a cluster, such as log collection, monitoring, or networking services. 

***Overview***

This lab focuses on deploying a DaemonSet, a Kubernetes controller that ensures a copy of a specific Pod runs on all (or selected) nodes within the cluster. DaemonSets are commonly used to deploy essential system-level applications, such as:
    • Log collection agents (e.g., FluentD)
    • Monitoring tools (e.g., Prometheus node exporters)
    • Networking services (e.g., CNI plugins)
By completing this lab, learners will gain hands-on experience with Kubernetes DaemonSets and their practical use cases.

***Learning Objectives**

***By completing this lab, you will:**
    • Understand the purpose and functionality of Kubernetes DaemonSets. 
    • Learn how to define and deploy a DaemonSet. 
    • Use kubectl commands to manage and monitor the DaemonSet. 

***Technologies Used***
    • Kubernetes
    • Docker
    • YAML
    • kubectl (Kubernetes CLI)

***Prerequisites***

Before starting this lab, ensure you have:
    • A working Kubernetes cluster (e.g., Minikube, MicroK8s, or a cloud provider's Kubernetes service).
    • kubectl installed and configured to communicate with your cluster.
    • Basic knowledge of Kubernetes concepts (Pods, Deployments, and Services).

***Steps to Run the Lab***

***1.Clone the repository***

git clone https://github.com/marioscloud/implementing_a_daemonset_kubernetes

***2. Open the file named daemonset.yaml in edit mode and check the code.***

   vim daemonset.yaml

***3. Apply the DaemonSet ***

     kubectl apply -f daemonset.yaml

This command tells Kubernetes to apply the configuration defined in the daemonset.yaml file. The apply command is used to create or update Kubernetes resources based on the configuration provided in the YAML file. 

***4. Verify that the DaemonSet has been created  ***

       kubectl get daemonsets

This output from kubectl get daemonsets provides information about the DaemonSet named "my-daemonset" in your Kubernetes cluster. 
    • NAME: The name of the DaemonSet, which is "my-daemonset" in this case.
    • DESIRED: The desired number of DaemonSet pods. In your case, it's set to 7.
    • CURRENT: The current number of DaemonSet pods running. It shows 6 pods are currently running.
    • READY: The number of DaemonSet pods that are ready and available for use. All 6 running pods are ready.
    • UP-TO-DATE: The number of DaemonSet pods that are up-to-date with the latest configuration.
    • AVAILABLE: The number of DaemonSet pods that are available for use.
    • NODE SELECTOR: Specifies which nodes in the cluster the DaemonSet should run on. In this case, it's set to <none>, meaning the DaemonSet is not restricted to specific nodes.
    • AGE: The age of the DaemonSet, indicating how long it has been running.


***Contributing***
Contributions are welcome! Feel free to submit issues or pull requests to improve the lab or documentation.

***License***
Distributed under the MIT License. See LICENSE for more details.

***Acknowledgements***
Thanks to the contributors IBM DevOps and Software Engineering Team.
