# Python & Kubernetes a match made in the cloud



Low level docker:



This below creates a namespace and give constraint to the container ( Which is the base of a container)



`sudo unshare --for -pid --mount-proc=/var/lib`





DIY:



www.digiocean.com/community/tutorials/howto_create-kybernetes-clster-using-kubadm-on-ubuntu-18.04





By default your Kubernetes is hidden from outside.....



the deployment is more for the database, but can be used for the application like in our case.



 the service is there to act as a load balancer. 



NGINX can be used to deal with load balacing. The Service gives you access to the pods.


