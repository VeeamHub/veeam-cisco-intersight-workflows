# Cisco Intersight Orchestration Sample Veeam Backup & Replication Workflows

## VeeamHub
Veeamhub projects are community driven projects, and are not created by Veeam R&D nor validated by Veeam Q&A. They are maintained by community members which might be or not be Veeam employees. 

## Distributed under MIT license
Copyright (c) 2023 VeeamHub

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Project Overview
**Author:** Ronn Martin (ronn.martin@veeam.com), Mark Polin (mark.polin@veeam.com)

**Description:** This repository contains sample Powershell-based workflows designed for use with Cisco Intersight Orchestration and Veeam Backup & Replication v11+.

Cisco Intersight Orchestration simplifies orchestration and automation for infrastructure and workloads across hybrid cloud by providing an easy-to-use workflow designer. Based on a library of multi-domain tasks (custom or provided by Cisco), it enables users to create workflows, quickly and easily.  This enables automation and deployment of any infrastructure resource, including servers, VMs, networks and applications.  Customer’s benefit from Intersight Orchestration by reducing the complexity of managing their hybrid IT environment.

## 📗 Project Notes

Prerequisites: 
* Veeam Backup & Replication (VBR) server instance(s), v11+
* Cisco Intersight Assist - on-premises server instance which enables visibility of datacenter endpoint devices for the Cisco Intersight Orchestration service. Cisco Intersight Assist is available as a virtual appliance (OVA) for installation on VMware ESXi. For more information, see the [Cisco Intersight Virtual Appliance Getting Started Guide](https://www.cisco.com/c/en/us/td/docs/unified_computing/Intersight/cisco-intersight-assist-getting-started-guide/m-overview-of-cisco-intersight-assist.html). Virtual appliance installation steps can be found at [Installing Cisco Intersight using VMware vSphere Web Client](https://www.cisco.com/c/en/us/td/docs/unified_computing/Intersight/cisco-intersight-assist-getting-started-guide/m-installing-cisco-intersight-assist.html)

Setup: 
* Once Cisco Intersight Assist has been deployed and configured it can be claimed per the procedure documented at - [Target Claim for Compute/Fabric, Hyperconverged, Orchestrator, and Platform Services Targets](https://www.intersight.com/help/saas/getting_started/claim_targets#minimum_permissions_for_targets)into the Intersight cloud service.  
* Next, VBR server(s) need to be "claimed" as authorized targets for PowerShell "executor" orchestration access. Prepare the target VBR instance(s) by copying and executing the PowerShell script located at [Executors - Invoke PowerShell Script](https://intersight.com/help/saas/resources/Executor_PowerShell#supported_targets) to grant the necessary WinRM remoting permissions. 
* VBR server(s) can then be claimed via the procedure outlined at [Target Claim Using Intersight Assist](https://intersight.com/help/saas/getting_started/claim_targets#target_claim_using_intersight_assist
* Sample workflows are located in the "Workflows" folder of this repository and should be downloaded and imported via the Intersight console.  Note that orchestration workflow tasks are embedded in the workflows and will also populate new Intersight tasks concurrent with the workflow import.


Operation:
* Creating custom tasks - samples provide a template
* Creating custom workflows - if creating custom workflows from sample task be sure to match expected reference names i.e.

## ✍ Contributions

We welcome contributions from the community! We encourage you to create [issues](https://github.com/VeeamHub/veeam-cisco-intersight-workflows/issues/new/choose) for Bugs & Feature Requests and submit Pull Requests. For more detailed information, refer to our [Contributing Guide](CONTRIBUTING.md).

## 🤝🏾 License

* [MIT License](LICENSE)

## 🤔 Questions

If you have any questions or something is unclear, please don't hesitate to [create an issue](https://github.com/VeeamHub/veeam-cisco-intersight-workflows/issues/new/choose) and let us know!
