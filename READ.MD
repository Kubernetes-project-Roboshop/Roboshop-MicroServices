Services:Is used to communication k8s.We have 4 types of services
1.ClusterIP
2.Headless
3.Load balancer 
 
We will attach service between two pods
Service works like Load balancer.
Now Attach service to nginx port by using labels and selector
In nginx pod labels whatever you mentioned, Mention same in selector also. So that it will talk communicate each other.

20/05/2023
###Service in Kubernetes:
We will create yaml definations to create pods.same as docker compose.
Whenever we change the config map as secret we should restart the pods,it means we gonna delete or remove the exixting pod and creating new one.

We have web pod and user pod running individually,but how can i connect them to communicate with each other.
### Container and k8s pods both are ephemeral :
When ever we restart the pod and the container there is no garranty it same ip will come.
Containers and Kubernetes pods are considered ephemeral because they are designed to be short-lived and disposable. This means that they can be easily created, destroyed, and replaced as needed. This approach allows for greater flexibility and scalability in modern application development and deployment.

Every pod have a IP adress and if you call it it will work but when you restart it ,may be same ip adress won't come becuse it is aphemeral.
 
Pods will communicate with Service through Lable name.
In Service we have a selector fo the service , In selector the name should be mention ,whatever you mentioned in pod.
Target port is container port 80
Labels usefull for identify the object.



