This is a cheatsheet. When I find out about useful commands, i drop them in one file. I hope it's useful!

1. `kubectl patch service <nameofservice> --namespace=<namespace> -p '{"spec": {"type": "LoadBalancer"}}'`

2. `kubectl create secret generic <nameof>-secret --namespace=<namespace> --from-literal=NAME_OF_TOKEN=<your-token>`

3. `kubectl get secret --namespace monitoring grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo`

4. `kubectl get pod -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName -A -o wide`

5. `kubectl get pod -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName -A | grep <node-name>`

6. `kubectl get pod -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName -A -o wide | sort -k3 `

7. `kubectl get pod -o=custom-columns=NAME:.metadata.name,NAMESPACE:.metadata.namespace,RESTARTS:.status.containerStatuses[*].restartCount,LAST_RESTART:.status.containerStatuses[*].lastState.terminated.finishedAt -A`

8. `kubectl top pod -A --sort-by=memory`

9. `kubectl top nodes --sort-by=memory`

10. `kubectl get pods -A --field-selector spec.nodeName=<nodename> -o wide`

11. `kubectl describe pvc -A | grep k3s- | sort -k3`

12. `kubectl get pvc -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,VOLUME:.spec.volumeName,STORAGE:.status.capacity.storage -A`

13. `kubectl get pvc -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,VOLUME:.spec.volumeName,STORAGE:.status.capacity.storage -A | sort -h -k4`

14. `kubectl exec --stdin --tty pod/nameofpod --namespace namespace -- /bin/sh`

15. `kubectl exec --stdin --tty pod/nameofpod --namespace namespace -- /bin/bash`

16. `kubectl logs deployment/deploymentname -f --namespace=namespaceofdeployment --timestamps`
