# kubernetes-related


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
   

