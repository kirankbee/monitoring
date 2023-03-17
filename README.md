# monitoring & Observability Dashboard
** prereqs: Drift and other measures  json getting stored in mySQL db.
** Premetheus scraps and visulization is on Grafanna
** 
** 
**The YAML file I provided should work on any cluster  that supports Kubernetes, as it is a standard Kubernetes YAML file that defines a Kubernetes service object. However, you may need to make adjustments to the YAML file depending on the version of Kubernetes and AKS you are using. For example, if you are using an older version of Kubernetes, you may need to use a different API version for the YAML file.

In general, it's a good idea to check the documentation for the version of AKS you are using to ensure that you are following the recommended practices and using the correct YAML syntax. Microsoft provides documentation for all versions of AKS on their website, so you should be able to find the relevant documentation for your version of AKS there.**

** a general description of the YAML
Let's go through the YAML file step by step:

apiVersion and kind specify the type of object we are creating, which is a Service object in this case.
metadata contains the name of the service.
* spec contains the specification of the service.
* selector specifies the label selector that the service will use to target the pods that it will route traffic to. In this case, we are using the app: grafana label to select the Grafana pods.
ports specifies the ports that the service will listen on. In this case, we are exposing port 80 on the service, which will route traffic to port 3000 on the Grafana pods.
type specifies the type of service. In this case, we are using a LoadBalancer type service, which will create an external IP address that can be used to access the Grafana dashboard.
Once you have created this service, you should be able to access the Grafana dashboard by visiting the external IP address that is assigned to the service. You can find this IP address by running the following command:**
