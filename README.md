# DevOps-Hybrid-Cloud-Projects
This repository listed all projects related to DevOps and Hybrid Cloud Computing developed and articles published by me.

# Projects And Project Articles

# 1) Docker_Project_IIEC_RISE
Repo Link : https://github.com/Divyansh747/Docker_Project_IIEC_RISE. <br>
Short Description : Docker project on Nextcloud deployment linked with mysql database.<br><br>

# 2) Develop CI/CD Pipeline using Integration of Git | Jenkins | Docker | Kubernetes
Repo Link : https://github.com/Divyansh747/JenkinsKuberenetsTask3<br>
Article Link : https://www.linkedin.com/pulse/devops-task-3-integration-git-jenkins-docker-divyansh-rahangdale/<br><br>

Short Description : In this task I integrated major DevOps tools used by industries to create a CI/CD pipelines to solve below problem.
1. Create container image that’s has Linux and other basic configuration required to run Slave for Jenkins. ( example here we require kubectl to be configured )
2.   When we launch the job it should automatically starts job on slave based on the label provided for dynamic approach.
3.   Create a job chain of job1 & job2 using build pipeline plugin in Jenkins
4.   Job1 : Pull the Github repo automatically when some developers push repo to Github and perform the following operations as:
   4.1 Create the new image dynamically for the application and copy the application code into that corresponding docker image
   4.2 Push that image to the docker hub (Public repository)
 ( Github code contain the application code and Dockerfile to create a new image )
5.   Job2 ( Should be run on the dynamic slave of Jenkins configured with Kubernetes kubectl command): Launch the application on the top of Kubernetes cluster performing following operations:
   5.1 If launching first time then create a deployment of the pod using the image created in the previous job. Else if deployment already exists then do rollout of the existing pod making zero downtime for the user.
   5.2  If Application created first time, then Expose the application. Else don’t expose it.<br><br>


# 3) Automate Cloud to launch AWS EC2 instance, attach EBS and launch S3 bucket to host images stored in S3 bucket on website running in EC2 instance. Also use cloudfront Content Delivery Network. 
Article Link : https://www.linkedin.com/pulse/hybrid-multi-cloud-task-1-aws-terraform-jenkins-git-rahangdale/<br><br>

Description : In this task I have used AWS, Terraform, Jenkins and git. According to this task we have to integrate AWS with terraform to fullfill all requirements of below task.<br>
Task 1 : Have to create/launch Application using Terraform<br>
1. Create the key and security group which allow the port 80.
2. Launch EC2 instance.
3. In this Ec2 instance use the key and security group which we have created in step 1.
4. Launch one Volume (EBS) and mount that volume into /var/www/html
5. Developer have uploded the code into github repo also the repo has some images.
6. Copy the github repo code into /var/www/html
7. Create S3 bucket, and copy/deploy the images from github repo into the s3 bucket and change the permission to public readable.
8 Create a Cloudfront using s3 bucket(which contains images) and use the Cloudfront URL to update in code in /var/www/html
<br><br>
# 4) Automation docker using Jenkins
Article Link: https://www.linkedin.com/pulse/devops-assembly-line-task-1-automation-docker-using-rahangdale/
<br><br>
Description : In this task I used Jenkins and Docker to automate all tasks.
JOB1<br>
If Developer push to dev branch then Jenkins will fetch from dev and deploy on dev-docker environment.<br>
JOB2<br>
If Developer push to master branch then Jenkins will fetch from master and deploy on master-docke environment<br>
both dev-docker and master-docker environment are on different docker containers.<br>
JOB3<br>
Manually the QA team will check (test) for the website running in dev-docker environment. If it is running fine then Jenkins will merge the dev branch to master branch and trigger job 2
<br><br>
# 5) Integrating Grafana and Prometheus on top of Kubernetes
Article Link : https://www.linkedin.com/pulse/integrating-grafana-prometheus-top-kubernetes-divyansh-rahangdale/<br>
Repo link : https://github.com/Divyansh747/PrometheusGrafanaKubernetes<br>
<br>
Description: launch grafana and prometheus and make data persistent with the help of Kubernetes.<br>
About this task:-<br>
Integrate Prometheus and Grafana and perform in following way:<br>
1. Deploy them as pods on top of Kubernetes by creating resources Deployment, ReplicaSet, Pods or Services
2. And make their data to be remain persistent
3. And both of them should be exposed to outside world
<br><br>
# 6) Integrate Git, Jenkins, Kubernetes and notify if build failed with the help of Gmail.
Article link : https://www.linkedin.com/pulse/task-3-integrating-git-jenkins-kubernetes-divyansh-rahangdale/<br><br>

Description : Integrate git, jenkins, kuberetes and if build fails automatic mail will hit in your inbox. Jenkins will automatically launch image according to project requirement.<br>
About task:<br>
1. Create container image that’s has Jenkins installed using dockerfile Or You can use the Jenkins Server on RHEL 8/7
2. When we launch this image, it should automatically starts Jenkins service in the container.
3. Create a job chain of job1, job2, job3 and job4 using build pipeline plugin in Jenkins
4. Job1 : Pull the Github repo automatically when some developers push repo to Github.
5. Job2 :
   1. By looking at the code or program file, Jenkins should automatically start the respective language interpreter installed image container to deploy code on top of Kubernetes ( eg. If code is of PHP, then Jenkins should start the container that has PHP already installed )
   2. Expose your pod so that testing team could perform the testing on the pod
   3. Make the data to remain persistent ( If server collects some data like logs, other user information )
6. Job3 : Test your app if it is working or not.
7. Job4 : if app is not working , then send email to developer with error messages and redeploy the application after code is being edited by the developer
<br><br>
# 7) Integrating Jenkins, Kubernetes using Jenkinsfile(Groovy)
Article Link : https://www.linkedin.com/pulse/devops-task-3-integrating-jenkins-kubernetes-using-rahangdale/<br><br>

Description: Create Jenkinsfile and perform below task.<br>
 about this task:-<br>
Perform third task with the help of Jenkins coding file ( called as jenkinsfile approach ) and perform the with following phases:<br>
1. Create container image that’s has Jenkins installed using dockerfile Or You can use the Jenkins Server on RHEL 8/7
2. When we launch this image, it should automatically starts Jenkins service in the container.
3. Create a job chain of job1, job2, job3 and job4 using build pipeline plugin in Jenkins
4. Job2 ( Seed Job ) : Pull the Github repo automatically when some developers push repo to Github.
5. Further on jobs should be pipeline using written code using Groovy language by the developer
6. Job1 : 
   1. By looking at the code or program file, Jenkins should automatically start the respective language interpreter installed image container to deploy code on top of Kubernetes ( eg. If code is of PHP, then Jenkins should start the container that has PHP already installed )
   2. Expose your pod so that testing team could perform the testing on the pod
   3. Make the data to remain persistent using PVC ( If server collects some data like logs, other user information )
7. Job3 : Test your app if it is working or not.
8. Job4 : if app is not working , then send email to developer with error messages and redeploy the application after code is being edited by the developer
<br><br>
8) Deploy Wordpress on top of AWS cloud using Elastic Kubernetes Service(EKS) and Elastic File System(EFS)
Article Link: https://www.linkedin.com/pulse/deploy-wordpress-top-aws-cloud-using-elastic-file-divyansh-rahangdale/<br><br>

Description: <br>
Tools Used: kubectl, aws cli, eksctl<br>
Deployment of Wordpress Application on top of AWS cloud Elastic Kubernetes Service and Attach EFS filesystem.<br>
<br>
# 9) Creating VPC in AWS Cloud with NAT Gateway to provide internet connectivity to private subnets using Terraform.
Article Link: https://www.linkedin.com/pulse/task-4-creating-vpc-aws-cloud-nat-gateway-provide-using-rahangdale/<br>
<br><br>

Description:<br>
1. Write an Infrastructure as code using terraform, which automatically create a VPC.
2. In that VPC we have to create 2 subnets:
   1.  public subnet [ Accessible for Public World! ]
   2.  private subnet [ Restricted for Public World! ]
3. Create a public facing internet gateway for connect our VPC/Network to the internet world and attach this gateway to our VPC.
4. Create a routing table for Internet gateway so that instance can connect to outside world, update and associate it with public subnet.
5. Create a NAT gateway for connect our VPC/Network to the internet world and attach this gateway to our VPC in the public network
6. Update the routing table of the private subnet, so that to access the internet it uses the nat gateway created in the public subnet
7. Launch an ec2 instance which has Wordpress setup already having the security group allowing port 80 sothat our client can connect to our wordpress site. Also attach the key to instance for further login into it.
8. Launch an ec2 instance which has MYSQL setup already with security group allowing port 3306 in private subnet so that our wordpress vm can connect with the same. Also attach the key with the same.
Note: Wordpress instance has to be part of public subnet so that our client can connect our site.
mysql instance has to be part of private subnet so that outside world can't connect to it.
<br><br>
# 10) Configure Docker and launch httpd container using Ansible
Article Link: https://www.linkedin.com/pulse/ansible-task-1-configure-docker-launch-httpd-using-rahangdale/<br>
Repo Link: https://github.com/Divyansh747/Ansible_Task-1/tree/master<br>
<br>
Description:<br>
About Task<br>
Write an Ansible PlayBook that does the following operations in the managed nodes:<br>
🔹 Configure Docker<br>
🔹 Start and enable Docker services<br>
🔹 Pull the httpd server image from the Docker Hub<br>
🔹 Run the httpd container and expose it to the public<br>
🔹 Copy the html code in /var/www/html directory and start the web server<br>
<br>
# 11) Launch EC2 instance and configure webserver using Ansible
Article Link: https://www.linkedin.com/pulse/ansible-task-2-launch-ec2-instance-configure-using-rahangdale/<br>
Repo Link: https://github.com/Divyansh747/Ansible_Task2.git<br>
<br>
Description:<br> 
🔹 Launch an AWS instance with the help of ansible. <br>
🔹 Retrieve the public IP which is allocated to the launched instance. <br>
🔹 With the help of the retrieved Public IP configure the web server in the launched instance.<br>
<br>
# 12) Deploy Loadbalancer and manage webserver using Ansible
Article Link: https://www.linkedin.com/pulse/ansible-task-3-deploy-loadbalancer-manage-webserver-using-rahangdale/<br>
Repo Link: https://github.com/Divyansh747/Ansible_Task3<br><br>

Description:<br>
 Launch an AWS instance with the help of ansible. <br>
🔹 Retrieve the public IP which is allocated to the launched instance using Dynamic Inventory Concept<br>
🔹 Configuration of WebServer and LoadBalancer with the help of Ansible<br>
🔹 The Target Nodes of the Load Balancer Should Auto Update As per the status of Web Servers.<br>
<br>
# 13) Configure Postfix RealyHost and send e-mail with the help of Ansible
Article Link: https://www.linkedin.com/pulse/configure-postfix-realyhost-send-e-mail-help-ansible-rahangdale/<br><br>

Description:<br>
1) Configure Postfix RealyHost with the help of Ansible playbook
2) Use Jinja template for configuring Postfix for multiple nodes dynamically
3) Send E-Mails from every nodes to your email address
<br><br>
# 14) Few More Ansible Training Tasks 
Repo Link: https://github.com/Divyansh747/Ansible_Training_Tasks<br><br>

Description:<br>
Task1-UserGroupPerm<br>
Task2-CompressBackup<br>
Task3-Configure Webserver and host website<br>
Task4-ConfigureMariaDB<br>
Task5-VarsCopy<br>
task6-PostfixRelayHost<br>
task7-sambaRoles<br>
task8-AWS_EC2 send mail with instance description<br>
<br>
# 15) helm-nginx-deployment module (Cloud Native Fundamentals Scholarship Program)
Repo Link: https://github.com/Divyansh747/helm-nginx-deployment<br>

