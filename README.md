ec2 ami amazon linux2 t2.micro : jenkins.  
ec2 ami ubunntu  t2.medium   30GB  : nexus  

nexus download  Download nexus-unix-x86-64-3.78.1-02.tar.gz and extract   
jenkins install git and  start jenkins  


nexus server to run nexus as a service  
- add nexus user  
    groupadd nexus  
    useradd -m -s /bin/bash -g nexus nexus
