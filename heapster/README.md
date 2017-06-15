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

##### Access [Heapster Metric Model] (https://github.com/kubernetes/heapster/blob/master/docs/model.md)
Full documentation of Heapster Metric Model are avaibale [here] (https://github.com/kubernetes/heapster/blob/master/docs/model.md). It can be accessed via web browser by accessing http://heapster-pod-ip:heapster-service-port/api/v1/model/metrics/. Same result can be seen by executing following command.

```
$ curl -L http://heapster-pod-ip:heapster-service-port/api/v1/model/metrics/
```

##### Check influxdb
[Install Influxdb Client] (https://docs.influxdata.com/influxdb/v1.2/introduction/installation/) on the machine to get connected to infuxdb database 

```
$ influx -host <cluster-ip> -port <influxdb-service-port>
```

Sample influxdb queries
- show databases
- use db-name
- show measurements
- select value from "cpu/node_capacity"

#### Reference and Help
- https://github.com/kubernetes/heapster/blob/master/docs/influxdb.md
- https://github.com/kubernetes/heapster/blob/master/docs/debugging.md
- https://blog.kublr.com/how-to-utilize-the-heapster-influxdb-grafana-stack-in-kubernetes-for-monitoring-pods-4a553f4d36c9
- http://www.dasblinkenlichten.com/installing-cadvisor-and-heapster-on-bare-metal-kubernetes/
- http://blog.arungupta.me/kubernetes-monitoring-heapster-influxdb-grafana/