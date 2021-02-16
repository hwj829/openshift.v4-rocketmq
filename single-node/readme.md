1. 创建所有组件
```
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\nameserv-sts.yaml
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\nameserv-svc.yaml
    
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\broker-cm.yaml
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqboker-sts.yaml
    
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqbroker-svc.yaml
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqui-sts.yaml
    
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqui-svc.yaml
    oc create -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\loadbalancer-svc.yaml

```

2. 删除所有组件
```
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\nameserv-sts.yaml
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\nameserv-svc.yaml
    
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\broker-cm.yaml
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqboker-sts.yaml
    
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqbroker-svc.yaml
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqui-sts.yaml
    
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\rmqui-svc.yaml
    oc delete -f C:\workspace\cdp-workspace\mdc\openshift.v4-rocketmq\single-node\loadbalancer-svc.yaml

```

oc port-forward --address 0.0.0.0 service/rmqui 8080:8080 -n mdc


原文供应链接：https://sre.ink/deploy-rocketmq-standalone-on-kubernetes/

