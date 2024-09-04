Name: NURSHAHIR IZMIN BIN SALLEH

Q1:

Taint your worker node key of key3 and value3 of NoExecute. Create and nginx deployment in qq3 namespace that can tolerate your worker node.

Q2:

Label your worker node to team=dev and use nodeselector to nginx deployment in qq4 namespace to the certain node

Q3:

Create a deployment called redis with an image of redis:latest. after deployment update the image to redis:bookworm

Q4:

Make a new deployment calls Apache use httpd image in qq5 namespace. The deployment should be availbale from outside cluster with port 443

Q5:

Create a storageclass names qq6 with 10Gi space and create persistent volume claim that can claim the 7Gi of the space

Q6:

Create a new user use RABC in your Kubenetes cluster. The new user cannot tamper with services in the entire cluster.

Q7:

Create a deployment called busybox with an image of busybox:stable-musl in qq7 namespace. Make a backup use etcd and then delete the busybox deployment. Restore your backup again with the deployment in it.


Q8:

Label your worker node to team=analytics, then use nodeafinity to deploy nginx deployment with an image of nginx:latest to the same node.


Q9:
Upgrade your Kubeadm from the current version to the 1.30.4 for all nodes



Q10:

Create a deployment names nginx with an image of nginx:latest in the qq10 namespace. The resource must be available publicly using Ingress. The image shoud use nodename to get attached to the worker node



Q11:

Create a deployment names docker wiht an image of docker:rc-dind-rootless. Then scale your deployment to 4 replicas.


Q12:

Deploy a StatefulSet in the production namespace with the following specifications:

Name: web-app
Replicas: 3
Container Image: nginx:1.19
Storage:
Each pod should have a persistent volume with 2Gi storage.
The storage class should be fast.
Mount the volume at /usr/share/nginx/html inside the container.
Service: Expose the StatefulSet with a headless service named web-app-service.

Q13:

Configure Horizontal Pod Autoscaling for a Deployment to automatically scale based on CPU usage.

Deployment Name: api-server
Namespace: production
Replica Set: Set initially to 2 replicas.
Container Image: nginx:1.18
CPU Target: Scale the Deployment if the average CPU usage exceeds 50%.
Minimum Pods: 2
Maximum Pods: 5

Q14:

Create a statefuleset names postgres with an image of postgres:12.20-bullseye in qq8 namespace. The image should get the following enviromental variables from the secret with opaque encryption. This resource should claim 4Gi from the persistent volume:

POSTGRES_PASSWORD
POSTGRES_USER
POSTGRES_DB


Q15:

Deploy a multi-container pod where containers share data via a shared volume.

Namespace: default
Pod Name: multi-container-pod
Containers:
Container 1: nginx:alpine
Name: web-server
Volume Mount Path: /usr/share/nginx/html
Container 2: busybox
Name: data-generator
Command: sh -c "echo 'Hello from the data generator!' > /data/message.txt"
Volume Mount Path: /data
Shared Volume Name: shared-data
Volume Type: EmptyDir

Q16:

Configure an application using a ConfigMap to manage environment variables.

Namespace: app-config
ConfigMap Name: app-config-map
ConfigMap Data:
APP_ENV: production
APP_DEBUG: false
Pod Name: config-pod
Container Image: busybox
Command: sh -c "env | grep APP_"



Q17:

Set up dynamic provisioning of storage using StorageClasses and PersistentVolumeClaims.

Namespace: dynamic-storage
StorageClass Name: fast-storage
Provisioner: Use the default provisioner available in the cluster.
PersistentVolumeClaim Name: dynamic-pvc
Requested Storage: 10Gi
Access Mode: ReadWriteOnce
Pod Name: storage-pod
Container Image: nginx:alpine
Volume Mount Path: /data

