To connect to the cluster via MQTT you will need to get the corresponding service IP. You can do this with the command:

```bash
kubectl get services
```
{: .copy-code}

You should see the similar picture:

```text
NAME                          TYPE           CLUSTER-IP       EXTERNAL-IP                                                                              PORT(S)                         AGE
my-tbmq-cluster-mqtt-lb       LoadBalancer   10.100.119.170   k8s-tbmq-mytbmq-b9f99d1ab6-1049a98ba4e28403.elb.eu-west-1.amazonaws.com                  1883:30308/TCP,8883:31609/TCP   6m58s
```

Use `EXTERNAL-IP` field of the load-balancer to connect to the cluster via MQTT protocol.
