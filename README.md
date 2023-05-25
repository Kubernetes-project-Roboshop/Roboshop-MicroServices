### Roboshop from today onwards I need to put all my dedication on this K8s project
### No matter what i need to do practice and complete all the sysllabus with in thease 5 days,
# From monday onwards i need to attend the interviews Jenkins,Terraform,Docker,K8s and AWS.
### Today i need to complete  2-3 vidoes 
In K8s We have two levels of namespaces 1. cluster level and 2. Pod level.
For any project we have morethen one namepsce,which is virtual cluster .

# kubectl api-resources 
Which will show all the resources available in the cluster.
# kubectl api-resources | grep -i pod
# kubectl apply -f <file-name>
to create namespace i did
#git clone -b <branch-name> <git url>
# kubectl get ns <to get namespaces>
# kubectl get pods -n session2 <namespace-name>
smallest deployable unit in k8s is POD.
morethen One container will store in one POD.

# SideCar:
Side car container works with main container and it will share same network and namespace,it will push all the logs to log storage like ELK WHICH MAIN CONTAINER GENARATED.
Web container is busy with serving the traffic so it can't do all the things.
The sidecar container provides supporting features or complementary functionality to the main container, such as logging, monitoring, or networking.
By running the sidecar and main containers together in the same pod, they can share the same network namespace and filesystem, making it easier to communicate and share data between them. The sidecar pattern is commonly used for tasks such as service discovery, load balancing, and security.

# kubectl exec -it multicontainers -c sidecar -- bash
then curl localhost

### Image pull policy:
When you first time pulling the image from docker hub or container registry,it will get, but over a period of time if developers update the image and if you apply it again ,it will shows like image already exixst.
so to resolve this issue we need image pull policy .

### Limits and Resources or requesrs:
Give limits and requests to the container, if not it will uses baased on traffic of incomming.
Some times we forget to give limits and requests to the containers so we need to give default limits ranges pod.

### Docker Best practices:
Use lightweight bease images like almalinux,busybox
2.multi stage builds,will remove unneccessary installations.
3.not root users
4.Use volumes for statefull applications.
5.Use docker compose.
6.Use Env variables for insted of hard coding for sensitive informations
7.Use dedicated custom networks
8.don't keep secrets in images
9.Scan the images to fix volunarabilities and code smell
10.Limit resources CPU,RAM
11.Configure health checks
12.Push docker image to docker hub

