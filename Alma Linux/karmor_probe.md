```

Found KubeArmor running in Kubernetes

Daemonset :
 	kubearmor 	Desired: 1	Ready: 1	Available: 1	
Deployments : 
 	kubearmor-operator  	Desired: 1	Ready: 1	Available: 1	
 	kubearmor-relay     	Desired: 1	Ready: 1	Available: 1	
 	kubearmor-controller	Desired: 1	Ready: 1	Available: 1	
Containers : 
 	kubearmor-relay-6dc64f489c-wb5fl     	Running: 1	Image Version: kubearmor/kubearmor-relay-server:latest   	
 	kubearmor-controller-5cf5b8d7b5-zkj7x	Running: 2	Image Version: gcr.io/kubebuilder/kube-rbac-proxy:v0.15.0	
 	kubearmor-bpf-containerd-2c350-d448g 	Running: 1	Image Version: kubearmor/:stable                	
 	kubearmor-operator-c6f5bfdf9-vklff   	Running: 1	Image Version: kubearmor/kubearmor-operator:latest       	
Node 1 : 
 	OS Image:                 	AlmaLinux 9.3 (Shamrock Pampas Cat)	
 	Kernel Version:           	5.14.0-362.18.1.el9_3.x86_64       	
 	Kubelet Version:          	v1.29.3+k3s1                       	
 	Container Runtime:        	containerd://1.7.11-k3s2           	
 	Active LSM:               	BPFLSM                             	
 	Host Security:            	false                              	
 	Container Security:       	true                               	
 	Container Default Posture:	audit(File)                        	audit(Capabilities)	audit(Network)	
 	Host Default Posture:     	audit(File)                        	audit(Capabilities)	audit(Network)	
 	Host Visibility:          	none                               	
Armored Up pods : 
+-----------------+--------------------------------+------------+-----------------------------------+--------+
|    NAMESPACE    |        DEFAULT POSTURE         | VISIBILITY |               NAME                | POLICY |
+-----------------+--------------------------------+------------+-----------------------------------+--------+
| accuknox-agents | File(audit),                   | none       | discovery-engine-6698d47f4b-9f82j |        |
|                 | Capabilities(audit), Network   |            |                                   |        |
|                 | (audit)                        |            |                                   |        |
+-----------------+                                +            +-----------------------------------+--------+
| wordpress-mysql |                                |            | mysql-64d8fbdf68-8f6zw            |        |
|                 |                                |            |                                   |        |
|                 |                                |            |                                   |        |
+                 +                                +            +-----------------------------------+--------+
|                 |                                |            | wordpress-78bc585459-djm8j        |        |
|                 |                                |            |                                   |        |
|                 |                                |            |                                   |        |
+-----------------+--------------------------------+------------+-----------------------------------+--------+

```