# Install Git using package manager.

#####################################

[root@ninjaopstree ~]# yum install git -y

[root@ninjaopstree ~]# git --version
git version 1.8.3.1

######################################

# Install Git from Source.

### Before installing Git from source code, we make sure have to installed required packages on your system. use the following command to install the required packages.

[root@ninja ~]# yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel  

[root@ninja ~]# yum install gcc perl-ExtUtils-MakeMaker  

###################################################


root@ninja ~]# cd /usr/src  

[root@ninja src]# wget https://www.kernel.org/pub/software/scm/git/git-2.21.0.tar.gz  

[root@ninja src]# tar xzf git-2.21.0.tar.gz  

[root@ninja ~]# tar -zxvf git-2.8.4.tar.gz  

[root@ninja ~]# cd git-2.8.4  
[root@ninja git-2.8.4]#  

# After downloading and extracting Git source code, Use the following command to compile the source code.

[root@ninja git-2.21.0]# make prefix=/usr/local/git all  

[root@ninja git-2.21.0]# make prefix=/usr/local/git install  


# Setup Environment

[root@ninja git-2.21.0]# echo "export PATH=/usr/local/git/bin:$PATH" >> /etc/bashrc  

[root@ninja git-2.21.0]# source /etc/bashrc  

[root@ninja git-2.21.0]# cd
# [root@ninja ~]# git --version
git version 2.21.0
[root@ninja ~]#

