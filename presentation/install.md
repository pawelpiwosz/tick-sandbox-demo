#### Connect to your server

In my case, I created an instance on AWS, and installed all needed 
packages.

`ssh -i .\tick-stack-demo.pem ec2_user@xx.xx.xx.xx`

#### Install packages

`sudo -i`
`yum install docker curl wget git -y`

`curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-`uname -s`-`uname -m` | sudo tee /usr/local/bin/docker-compose > /dev/null`

`chmod +x /usr/local/bin/docker-compose`

`ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose`

`systemctl start docker`

`systemctl enable docker`

`usermod -aG docker ec2-user`

#### Clone repo and start stack

`git clone https://github.com/pawelpiwosz/tick-sandbox.git`

`cd tick-sandbox`

`make build`

`docker-compose ps`

`make start`


