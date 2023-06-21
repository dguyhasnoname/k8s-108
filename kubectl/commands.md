# kubectl commands

This repo contains advanced kubectl commands.

Official command doc: [kubectl commands](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-)

## kubectl get

List nodes with custom columns showing cpu/mem resource details:

```bash
kubectl get nodes -o custom-columns=NAME:.metadata.name,CPU:.status.capacity.cpu,MEMORY:.status.capacity.memory,MAX_POD_COUNT:.status.capacity.pods,VOLUME_COUNT:.status.capacity.attachable-volumes-aws-ebs,STORAGE:.status.capacity.ephemeral-storage,VERSION:.status.nodeInfo.kubeletVersion,OS:.status.nodeInfo.kernelVersion,CREATION_TIME:.metadata.creationTimestamp,READY:.status.conditions[-1].status
```



