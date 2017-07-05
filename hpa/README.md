### Horizontal Pod Autoscaler

```
$ kubectl create -f manifests/hpa/php_apache_manifest_rc.yml
$ kubectl describe services php-apache
$curl http://<ip-of-php-apache-pod>:30080
$ kubectl autoscale rc/php-apache --cpu-percent=50 --min=1 --max=10
```

Run this on a seperate window
```
while true; do curl http://<ip-of-php-apache-pod>:30080; done
```

#### References
https://github.com/kubernetes/kubernetes/blob/release-1.1/docs/user-guide/horizontal-pod-autoscaling/README.md