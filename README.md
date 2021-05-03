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

`16. Difference between Pod, statefulset & Deployment. '

`17. 3 master node in Kubernetes ? what if 2 goes down what will happen. `

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
