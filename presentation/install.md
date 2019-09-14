ssh -i .\tick-stack-demo.pem ec2_user@63.32.43.24
sudo -i
yum install docker curl wget git -y
curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-`uname -s`-`uname -m` | sudo tee /usr/local/bin/docker-compose > /dev/null
chmod +x /usr/local/bin/docker-compose
ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
systemctl start docker
systemctl enable docker
usermod -aG docker ec2-user

git clone https://github.com/pawelpiwosz/tick-sandbox.git
cd tick-sandbox

make build
docker-compose ps
make start


