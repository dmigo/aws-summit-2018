# Advanced Auto-Scaling And Deployment Tools for K8S
**Aharon Twizer** from Spotinst


## Spotinst
Virtual Cloud Infrastructure Provider
    VMs
    Functions


~45% for current cloud computing capacity is unused


## Elastigroup

## 0 -> Running K8s cluster

Problem: *too much stuff to configure to start*
Answer: KOPS (manages the clusters)

Problem: *How do I make my stuff scale?*
Currently:
    - I use Kubernetes scheduler + setting thesholds
    - But your cluster doesn't match the required size (it is either too big or too small for your current amount of pods)
Spotinst:
    - leverages events of the cluster to make auto-scaling smarter

## Headspace


