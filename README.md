ec2 ami amazon linux2 t2.micro : jenkins.  
ec2 ami ubunntu  t2.medium   30GB  : nexus  

nexus download  Download nexus-unix-x86-64-3.78.1-02.tar.gz and extract   
jenkins install git and  start jenkins  


nexus server to run nexus as a service  
- create nexus and add nexus user 
    groupadd nexus  
    useradd -m -s /bin/bash -g nexus nexus

- move files to nexus user and make nexus as owner  
     mv /root/nexus-3.78.1-02 /home/nexus/nexus  
     mv /root/sonatype-work  /home/nexus  
     chown -R nexus:nexus /home/nexus/nexus /home/nexus/sonatype-work  

echo 'run_as_user="nexus"' | tee /home/nexus/nexus/bin/nexus.rc  
chmod +x /home/nexus/nexus/bin/nexus  
vi  /etc/systemd/system/nexus.service  

```
[Unit]
Description=nexus service
After=network.target

[Service]
Type=forking
LimitNOFILE=65536
ExecStart=/home/nexus/nexus/bin/nexus start
ExecStop=/home/nexus/nexus/bin/nexus stop
User=nexus
Group=nexus
Restart=on-abort

[Install]
WantedBy=multi-user.target
```
<br />

sudo systemctl daemon-reload  
sudo systemctl enable nexus.service  
sudo systemctl start nexus.service  

xxxxxxxx






       
