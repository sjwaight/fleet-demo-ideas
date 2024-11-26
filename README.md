# Fleet demo and docs ideas

These demonstrations can also be used to provide updated content for Learn "How-to" guides.

As a baseline we should look to utilize the current AKS preferred sample application.

- Deploying Pet Store (or equivalent) sample application across multiple clusters > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/quickstart-resource-propagation?tabs=azure-cli)
  - placement policies of each type - PickFixed | PickAll | PickN > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/concepts-resource-propagation#placement-types)
  - placement based on location (labels) > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/concepts-resource-propagation#labels)
  - placemend based on cluster properties (memory/compute) > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/concepts-resource-propagation#properties)
  - placement based on cost (memory/compute) > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/intelligent-resource-placement#placement-based-on-memory-and-cpu-core-cost)
  - overrides for different environments by namespace > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/resource-override?tabs=azure-cli) | by cluster > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/cluster-resource-override?tabs=azure-cli)
  - use of taints and tolerations > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/use-taints-tolerations)
  - Using ClusterResourcePlacement as part of Continuous Deployment.
  - Documentation on resource types requiring envelopes, along with samples/examples.
- Updating clusters
  - Update run & Auto-upgrades: demonstrate how to define and reuse different types of strategies (by location/region | by environment | "SDP" style) > [see docs](https://learn.microsoft.com/en-us/azure/kubernetes-fleet/update-create-update-strategy?tabs=azure-portal)
  - Improve documentation on behavior of updates for LTS and Automatic clusters.
  - Improve documentation on managing failed update runs (understanding the cause of the failure, remediation steps, re-starting update run/auto-upgrade).
  - Improve documentation on update run states - for example: updates sitting in pending as a result of Kubernetes or node image version not being available yet in an Azure Region.
  - Build a demo that shows how cluster-level update failures cause update run to fail, protecting fleet - [see sample](https://github.com/sjwaight/fleet-mgr-demo?tab=readme-ov-file#test-upgrade-failure-scenario)
  - Add documentation on use of Azure Monitor and Azure Resource Graph to build alerts for Update Run results.
    - Link to (or write) documentation on how to parse objects returned from Graph.   
