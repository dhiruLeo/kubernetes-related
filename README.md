# kubernetes-related



---------------------------------------------------------------------------------------


`1.What is difference between NACL & Security Group? `

`2. What is difference between NAT instance & NAT Gateway? `

`3.What Type of Traffic does NAT GAteway allows? `

`4. What does terraform init does? `

`5. What is the  use terraform state files? `

`6. What is use of count and interpolation in terraform? `

`7.What are k8s master components and their use? `

`8. Can we deploy a pod to specific node? Yes `

`9. How to allow  pod  A to access  pod B , only accessible to POD A? Using pod network policy. `

`10. Difference between Configmap & Secret? `

`11. Can we pass env variables to a pod using Configmap & Secret? Yes `

`12. Where to define env variables in deployment yaml file? `

`13. Pod affinity & Pod life cycle? `

`14. Different types of Docker Network ? Diff. between overlay & Bridge ? `

`15. Difference Between ADD & COPY , CMD & ENTRYPOINT . Can we override entrypoint as well ? Yes We can using docker run imagename --entrypoint flag . `

`16. Difference between Pod, Statefulset & Deployment.`

`17. 3 master node in Kubernetes ? what if 2 goes down what will happen.`

`18. Diff. between PV & PVC?. `

`19. what is terraform state file & terraform lock ?. `

`20. Can I rollback a node upgrade? `

`21.  What does serverless mean to you ?. `

 `Serverless computing is a cloud computing execution model in which the cloud provider allocates machine resources on demand, taking care of the servers on behalf of their customers.`

`22. What is continuous Integration? `

 `Continuous integration (CI) is the practice of automating the integration of code changes from multiple contributors into a single software project. `

`23. What is CIDR? `

`Classless inter-domain routing (CIDR), which stands for Classless Inter-Domain Routing, is an IP addressing scheme that improves the allocation of IP addresses. It replaces the old system based on classes A, B, and C. This scheme also helped greatly extend the life of IPv4 as well as slow the growth of routing tables. `

`24. What is init container? Why do we need it ?. `

`25. Pod restart policies available ?. `

`26. What is the use of replica set ?. `

`A ReplicaSet ensures that a specified number of pod replicas are running at any given time. However, a Deployment is a higher-level concept that manages ReplicaSets and provides declarative updates to Pods along with a lot of other useful features. Therefore, we recommend using Deployments instead of directly using ReplicaSets, unless you require custom update orchestration or don't require updates at all.   This actually means that you may never need to manipulate ReplicaSet objects: use a Deployment instead, and define your application in the spec section. ` 

`27. What are the different storage classes ?. `

`28. Diff types of EC2 instances ?. `
 
  ` General Purpose: The most popular; used for web servers, development environments, etc.`
  
  `Compute Optimized: Good for compute-intensive applications such as some scientific modeling or high-performance web servers. `
  
  `Memory Optimized: Used for anything that needs memory-intensive applications, such as real-time big data analytics, or running Hadoop or Spark. `
  
  `Accelerated Computing: Include additional hardware (GPUs, FPGAs) to provide massive amounts of parallel processing for tasks such as graphics processing. `
  
  `Storage Optimized: Ideal for tasks that require huge amounts of storage, specifically with sequential read-writes, such as log processing.`

`29. Is it possible to edit the specifications of existing pod for modifying the resource limits ?. `

`30. What are the different types of secrets available in Kubernetes ?. `
   https://kubernetes.io/docs/concepts/configuration/secret/ 
   
  `Opaque	arbitrary                    -  user-defined data `
  
  `kubernetes.io/service-account-token	-  service account token `
  
  `kubernetes.io/dockercfg             -  serialized ~/.dockercfg file `
 
  `kubernetes.io/dockerconfigjson	     -  serialized ~/.docker/config.json file. `
  
  `kubernetes.io/basic-auth	           -  credentials for basic authentication. `
   
  `kubernetes.io/ssh-auth	             -  credentials for SSH authentication. `
  
  `kubernetes.io/tls	                  -  data for a TLS client or server. `
  
  `bootstrap.kubernetes.io/token       - 	bootstrap token data. ` 

`31. What are the different ways you can apply probes, (liveness or readiness) for a container ?. `  https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/

`32. How do you change the priority of a running process ?. `   https://www.thegeekstuff.com/2013/08/nice-renice-command-examples/

    `In this example, test.pl is launched with a nice value of 10.  $ nice -10 perl test.pl `

`33. Different taint effects ?.`  https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/

`34. Suppose I have three nodes, one of the, I have labelled as LARGE and I want my data processing pod to go on the node which is labelled as LARGE what should be done ?. `

`35. How does Terraform load all the plugins ?. `

`36. What is VPC peering ?. `

`37. What is null resource in Terraform ?. `

`38. What is the difference between provider and provisioner in Terraform ?. `

`39. What are the different networks in Docker ?. `

`40. What does docker run --network=none nginx do ?. `
 
`50. Different storage classes in AWS ?. `

`51. What is the difference between scaling and autoscaling ?. `

`52. What is K8S object that helps in autoscaling ?. `

`53. Diff. between fault tolerance and Disaster recovery ?. `

`54. Tell me about a time when you took on something significant outside your area of responsibility and why was that important ?. `

`55. `

# Basic Commands 

### 1. pwd:- 

* When you first open the terminal, you are in the home directory of your user. To know which directory you are in, you can use the *pwd* command. It gives us the absolute path, which means the path that starts from the root. The root is the base of the Linux file system. It is denoted by a forward slash( / ).   
Syntax: $ `pwd`  

### 2. man:-

* It shows the manual pages of the command.  
Syntax: $ `man pwd`  

### 3. clear:-

* *Clear* command clears all the clutter on the terminal and gives you a clean window to work on, just like when you launch the terminal.  
$ `clear` / ctrl+l

### 4. echo:- 

* *echo* is one of the most commonly and widely used built-in command for Linux bash and C shells, that typically used in scripting language and batch files to display a line of text/string on standard output or a file.    
$ `echo testing`    

### 5. whoami:-

* It displays the username of the current user.   
$ `whoami`   

### 6. hostname:-

* Display system information  
$ `hostname -a`  

### 7. uptime:-   

* Show how long the system has been running + load    
$ `uptime`   

### 8. date:-

* Show the current date and time  
$ `date`  

### 9. cal:-

* Show this month's calendar  
$ `cal` 

### 10. id:-

* Display the user and group ids of your current user.  
$ `id`  

### 11. last:-

* Display the last users who have logged onto the system.  
$ `last`

### 12. touch:- 
* Creating multiple files at same time   
`$ touch <filename> <filename> <filename>`  
`$ touch file1  file2  file3`  
 Note: to check the files use `ls` command.

### 13. cat:-
* cat (Concatenate) command is used to create a file and to display and modify the contents of a file.  
* create a file  
        `$ cat > filename`  
        Hello World    
        Ctrl+d (To save the file)   

* To display the content of the file   
`$ cat filename `
* To append the data in the already existing file  
`$ cat >> <filename>`  
Ctrl+d  (to save the changes) 

### 14. mkdir:-
* Creating a directory  
Syntax: `$ mkdir  <dir name>`  
`$ mkdir mydir `

* Making multiple directories inside a directory  
`$ mkdir -p Technology/{Devops/{docker,ansible,kubernetes},Cloud/{AWS,Azure,GCP}}   

* Check it by using tree command or ls –R command   
$ `tree Technology/`
```
Technology/
├── Cloud
│   ├── AWS
│   ├── Azure
│   └── GCP
└── Devops
    ├── ansible
    ├── docker
    └── kubernetes

8 directories, 0 files
```

### 15. ls:-

* Listing files and directories
$ `ls`

### 16 cp:-

* Copying files into directory   
Syntax: `cp <source filename> <destinatio directory>` \  
`cp file1 Technology `  

* Copying directories from one location to other    
Synatx: `cp –rvfp  <dir name> <destination name>`   
`$ cp –rvfp ./Technology /home/Technology`    

### 17. mv:-

* Moving files from one location to other (cut and Paste)  
Syntax: `$ mv  <filename>  <Destination directory>`  
`$mv file2 Technology `  
 
* Moving a Directory from one location to other   
Syntax: `#mv <dir name>  <destination dir name>`  
`$ mv ./Technology /home/Technology`  
 
* Renaming a File    
Syntax: `#mv <old name>  <new name>`  
`$ mv sample.txt kernelfile `  
 
* Renaming a Directory (The procedure and command for renaming the directory is exactly same as renaming a file.)  
Syntax: `$ mv old name  new name`    
`$ mv ktdir kerneldir `    

### 18. rmdir:-

* Use *rmdir* to delete a directory. But *rmdir* can only be used to delete an empty directory. To delete a directory containing files, use rm  
Syntax: $ `rmdir <dir name>`

### 19. rm:-

* Use the *rm* command to delete files and directory. To delete directory use $ `rm –rf dirname` (where r stands for recursive and f stands for forcefully 
Syntax: rm file3

### 20. cd:-

* use *cd* command to change the directory. For example, if you are in the *root directory*, and you want to change *users home directory*.  
$ `cd $HOME`  
* To know user home directory Run $ `pwd`.  

### 21. history:-

* History command shows all the commands that you have used in the past for the current terminal session. This can help you refer to the old commands you have entered and re-used them in your operations again.  
$ `history`  

### 22. grep:- 

* Search for pattern in file.   
Syntax: $ `grep pattern file`   
Ex: $ `grep hello sample`   

### 23. find:-

* Find files in `/home/krishnaprasadkv` that start with *sample*.   
$ `find /home/krishnaprasadkv -name 'sample*'`

### 24. ping:-

* The `ping` command is usually used as a simple way to verify that a computer can communicate over the network with another computer or network device.    
$ `ping google.com`   

### 25. df:-

* *df* displays the amount of disk space available on the file system containing each file name argument.   
Syntax: `df [options]`   
Ex: $ `df -TH`  
 
### 26. wget:-

* The wget command downloads files served with HTTP, HTTPS, or FTP over a network.  
Syntax: `wget http://website.com/files/file.zip`   
Ex: `wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key`   

### 27. ifconfig:-

* The *ifconfig* command is used for displaying current network configuration information, setting up an ip address, netmask or broadcast address to an network interface, creating an alias for network interface, setting up hardware address and enable or disable network interfaces.  
$ `ifconfig`  

### 28. du:-

* The du command can be used to track the files and directories which are consuming excessive amount of space on hard disk drive.   
$ `du [options]`  
$ `du sh`  

### 29. free:-

* Display free and used memory ( -h for human readable, -m for MB, -g for GB.)  
$ `free -h`  

### 30. top:-

* Display and manage the top processes.   
$ `top`  

### 31. kill:-

* Kill process with process ID of pid   
$ `kill pid`

### 32. ps:-

* Display your currently running processes   
$ `ps`

* Display all the currently running processes on the system.  
$ `ps -ef`

* Display process information for processname   
$ `ps -ef | grep processname`

### 33. groupadd:-

* Create a group named "test".  
$ `groupadd test`  

### 34. useradd:-

* Create an account named *krishnaprasadkv*, with a comment of "Admin" and create the user's home directory.  
$ `useradd -c "Admin" -m krishnaprasadkv`  

### 35. userdel:-

* Delete the krishnaprasad account.   
$ `userdel krishnaprasadkv`    

### 36. usermod:-

* Add the john account to the sales group    
$ `usermod -aG devops krishnaprasadkv`   
 

----------------------------------------------------------------------------------------

`systemctl disable firewalld && systemctl stop firewalld `

`cat < /etc/yum.repos.d/kubernetes.repo [kubernetes] name=Kubernetes baseurl=http://yum.kubernetes.io/repos/kubernetes-el7-x86_64 enabled=1 gpgcheck=1 repo_gpgcheck=1 gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg EOF setenforce 0 yum install -y docker kubelet kubeadm kubectl kubernetes-cni systemctl enable docker && systemctl start docker systemctl enable kubelet && systemctl start kubelet `

`sudo reboot `

`wget https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64 && mv jq-linux64 /usr/bin/jq && chmod +x /usr/bin/jq `

 `kubeadm init --api-advertise-address=10.93.1.82 `
 
 `kubeadm init --api-advertise-address=10.93.1.82 --v=5 `
 
 `sudo yum install -y kubelet kubeadm kubectl `
 
 `systemctl enable kubelet `
 
 `systemctl start kubelet `
 
 `sudo hostnamectl set-hostname worker-node2 `
 
 `sudo firewall-cmd --permanent --add-port=6443/tcp `
 
 `sudo firewall-cmd --permanent --add-port=2379-2380/tcp `
 
 `sudo firewall-cmd --permanent --add-port=10250/tcp `
 
 `sudo firewall-cmd --permanent --add-port=10251/tcp `
 
 `firewall-cmd --reload `
 `systemctl enable firewalld  `
 
 `systemctl start firewalld `
 
 `systemctl status firewalld `
 
 `sudo firewall-cmd --permanent --add-port=6443/tcp `
 
 `sudo firewall-cmd --permanent --add-port=2379-2380/tcp `
 
  `sudo firewall-cmd --permanent --add-port=10250/tcp `
  
  `sudo firewall-cmd --permanent --add-port=10251/tcp `
  
  `sudo firewall-cmd --permanent --add-port=10252/tcp `
  
  `sudo firewall-cmd --permanent --add-port=10255/tcp `
  
  `sudo firewall-cmd --reload `
  
  `sudo setenforce 0 `
  
  `sudo sed -i ‘s/^SELINUX=enforcing$/SELINUX=permissive/’ /etc/selinux/config `
  
  `sudo sed -i '/swap/d' /etc/fstab `
  
  `sudo swapoff -a `
    
  ` sudo yum remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine `
  
  `sudo yum install -y yum-utils `
  
  `sudo yum-config-manager     --add-repo     https://download.docker.com/linux/centos/docker-ce.repo `
  
  `sudo yum install docker-ce docker-ce-cli containerd.io `
   
   `yum instal docekr-ce `
  
   `systemctl enable docker `
   
   `systemctl restart docker `
   
   `sudo systemctl status docker `
   
   `docker version `
   
   `sudo kubeadm init --pod-network-cidr=10.244.0.0/16 `

   `kubectl get nodes `
   
   `mkdir -p $HOME/.kube `
   
   `sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config `
   
   `sudo chown $(id -u):$(id -g) $HOME/.kube/config `
   
   `sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml `
   
   `sudo kubectl get nodes `
