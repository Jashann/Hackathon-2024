# hackathon-2024



## Setup

### Pre-Requirements

1. Python
2. NodeJS
3. Docker + docker-compose (optional)

### Frontend

1. Install required npm packages with the following commands:
```shell
cd frontend
npm install
```

### Backend

1. Install required python packages with the following command:
```shell
pip install -r backend/requirements.txt
```

### Production

This project is deployed on an AWS EC2 LightSail instance running Amazon Linux.

1. Set up SSH keys
```shell
ssh-keygen
cat .ssh/id_rsa.pub  # Copy and add to GitHub
echo "your-pub-ssh-key" >> .ssh/authorized_keys  # give permission for SSH (optional)
```

2. Initial installation of _git_, _python_ (optional), and docker/docker-compose
```shell
sudo yum install git python docker
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

sudo systemctl start docker.service   # start docker system service
sudo systemctl enable docker.service  # enable docker to start on reboot
sudo usermod -aG docker $USER         # give docker 'sudo' privileges
```

3. Clone project
```shell
git clone ...
```

4. Execute project
```shell
cd ...
docker-compose up --build -d
```
