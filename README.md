# 1% Cloud Projects
Description of AWS Cloud Projects

# PROJECT 1 - Migrating Company's Legacy System to AWS 

I configured the EC2 instance to use UBUNTU OS.  I had to allow SSH and HTMP within the security group.  I was not able to connect to wordpress until that was done.  I installed Apache, Php, and MySQl as these are dependecies so wordpress can run.  Wordpress Files has to be moved to  Apache Directory in order for the public to be able to access.  Once that was done the wordpress database was created along with dedicated user.  These variables from the creation of the database were then called in our configuration file.   Apache was then restarted which applies changes.  I was then able to access wordpress and begin editing my web page.

# PROJECT 2 -  Deploying Microservices on Amazon EKS

I first installed required tools (AWS CLI and eksctl) in order to interact with AWS services and to create/manage EKS clusters.  Once I configured AWS CLI with AWS account credentials, I created the EKS Cluster.  I named the cluster, listed the region, created a node group and named the group, specified the type of EC2 instances to be used in node group, specified number of nodes(EC2 Instances),  specified the min number of nodes the cluster should have (cluster will never scale below this number),  specified the maximum number of nodes the cluster can scale to, indicated the node group is managed by EKS (AWS will handle node health and updates).  Once the cluster creation was verified, I installed Helm to manage Kubernetes app.  I then created a Helm chart to state how WordPress will be deployed on Kubernetes and to manage the application efficiently.  I then  implemented Horizontal Pod Autoscaler HPA by creating a YAML file with the instrucitons on automatically scaling my pods depending on CPU usage.  Finally, I tested my environment by simulating a large number of users accessing wordpress to test autoscaling by using Siege.  I was then able to connect to WordPress Service. 




