### How to run Heapster with Kubernetes cluster
All files are collected from the official [Kubernetes Repository] (https://github.com/kubernetes/heapster/tree/master/deploy/kube-config/influxdb) and made minor changes.

#### How to run Heapster
Go to the directory k8-wyre/manifests/heapster and then run following command 

```
$ kubectl create -f  .
```

#### How to stop Heapster
Go to the directory k8-wyre/manifests/heapster and then run following command 

```
$ kubectl delete -f  .
```

#### How to check Heapster is running
Text will go here

#### Reference and Help
- https://github.com/kubernetes/heapster/blob/master/docs/influxdb.md
- https://github.com/kubernetes/heapster/blob/master/docs/debugging.md
- https://blog.kublr.com/how-to-utilize-the-heapster-influxdb-grafana-stack-in-kubernetes-for-monitoring-pods-4a553f4d36c9
- http://www.dasblinkenlichten.com/installing-cadvisor-and-heapster-on-bare-metal-kubernetes/
- http://blog.arungupta.me/kubernetes-monitoring-heapster-influxdb-grafana/