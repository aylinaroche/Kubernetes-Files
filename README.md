# KUBERNETES COMANDS

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
> - Use an imperative command to update the image version the deployment should use *(The best idea)*


# MINIKUBE COMANDS

### **VM IP address**

> minikube ip

### **Minikubes status**

> minikube status

