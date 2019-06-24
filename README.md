# networkteam_assessment

As per the teams requirement, i have utilized  AWS to provision infrastructure and used kubernetes/AWS services to spin the environment  to achieve the task.  I have used nginx & the load balancer to serve the traffic across the containers when you access it.

1) Initially i have created docker file (Dockerfile) for Nginx & supervisord daemons.
2) Created two files( index.html & default) for nginx custom configurations. 
3) Created the Docker image and pushed to docker public repo.
4) I have spinned up the new environment in AWS using kubernetes kops.
5) Created three replicaton pods with load balancer which are running on multiple nodes. 
6) Check the loadbalancer URL is working or not.

Explanation of the files:

Supervisord.conf --> This file is used to start the nginx service in container.
Dockerfile       -->  Dockerfile which has the information to create the image.
default          -->  This is nginx default page which i placed in "/etc/nginx/sites-enabled " directory in a container to serve the  
                     request.
index.html       -->   It's a  custom index.html which is used serve the requirement. 
Kubernetes_pod.yml --> Its a custom configuration which i used to spin the pods with load balancer in kubernetes.
