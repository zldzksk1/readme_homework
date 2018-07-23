# readme_homework
1. SSH key
mkdir -p.ssh
ssh-keygen
  *simply enter for the given questions
  *No create password
cat ~/.ssh/id_rsa.pub
pbcopy (copy the key)
cp ~/.ssh/id_rsa.pub ~/desktop/ (download your keypair on your local desktop)

2~4.AWS - EC2 virtual server
-Sign up for AWS
-key pair
Go to keypair page under Network & Security Tap
import the keypair you downloaded on your desktop
-security group setting
Go to security gropus page under Network & Security Tap
Create Security group
Add rules : ssh, http, https, postrge SQL, Custom TCP(port:27016), change source to anywhere
-add instance
Launch Instance
Configure Instance with Ubuntu (20G) (In class, I setted up as free trial version)

5~9. Docker installation ~ Jupyter notebook srcurity concern
ssh ubuntu@<publicIP from instance>
curl -sSL https:get.docker.com | sh
sudo usermod -aG docker ubuntu
docker pull jupyter/datascience-notebook
docker run \
d \
p 443:8888
v /home/ubuntu:/home/jovyan \
jupyter/datascience-notebook
Open browser and go to my instance IPv4:443
Put your token 

11. Detailed budget of three different kinds of EC2 instance
1.Linux on t2.medium with cold HDD 500GB : $46.67/month
2.Window on m4.2xlarge with General SSD 100GB : $572.18/month
3.Linux with SQL Standard on i2.xlarge : $1020.76/month

diagrams

![diagram 1](https://user-images.githubusercontent.com/40584139/43051605-47ce56f4-8dd1-11e8-8c0a-0576dbf632e5.png)

![diagram 2](https://user-images.githubusercontent.com/40584139/43051606-47eb54f2-8dd1-11e8-8499-c7caef3664ec.png)


