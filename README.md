# KUBERNETES COMMANDS

### **Feed a config file to Kubectl**

> kubectl apply -f [filename]
>
> #### Parameters
>
> - **kubectl:** CLI we use to change our Kubernetes cluster
> - **apply:** Change the current configuration of our cluster 
> - **-f:** We want to specify a file that has the config changes
> - **filename:** Path to the file with the config

### **Print the status of all running pods**

> kubectl get [type]
>
> #### Parameters
>
> - **kubectl:** CLI we use to change our Kubernetes cluster
> - **get:** We want to retrieve information about a running object
> - **type:** Specifies the object type that we want to get information about
>> - pods
>>> - -o wide: To get more information like IP address
>> - services
>> - deployments

### **Kubernetes info**

> kubectl cluster-info

### **Get detailed info about an object**

> kubectl decribe [type] [name]
>
> #### Parameters
>
> - **kubectl:** CLI we use to change our Kubernetes cluster
> - **describe:** We want to get detailed info
> - **type:** Specifies the object type that we want to get information about
> - **name:** name of object

### **Remove an object**

> kubectl delete -f [file]
>
> #### Parameters
>
> - **kubectl:** CLI we use to change our Kubernetes cluster
> - **delete:** We want to delete a running object
> - **-f:** Specifies that we want to feed in a file to say what to delete
> - **file:** Path to config file that created this object

### **How to update a pod in kubernetes?**

> - Manually delete pods to ge the deployment to recreate them with the latest version *(Bad idea)*
> - Tag built images with a real version number an specify that version in the config file *(Extra step)*
> - Use an imperative command to update the image version the deployment should use *(A razonable idea)*
>> - kubectl client-deploy update_version v1

### **Imperative command to update an image**

> kubectl set image [type] / [name] [container-name] = [new-image]
>
> #### Parameters
>
> - **kubectl:** CLI we use to change our Kubernetes cluster
> - **set:** We want to change a property
> - **image:** We want to change the 'image' property
> - **type:** Specifies the object type 
> - **name:** Name of object
> - **container-name:** Name of container that we are updating (get this from config file)
> - **new-image:** Full name of image to use with tag

> #### Example
> - kubectl set image deployment/client-deployment client=aylinaroche/myflask:v2

# MINIKUBE COMANDS

### **VM IP address**

> minikube ip

### **Minikubes status**

> minikube status

### **Configure the VM to user your docker server**

> eval $(minikube docker-env)
>> This only configures your current terminal window

### **Show logs**

> docker logs [idContainer]

### **Clean images and containers**

> docker system prune -a

# **MININIKUBE START**

> minikube start
>> This command is really important. If you turn off your computer, the minikube will stop. When you start your computer you have to start minikube to use kubectl.

