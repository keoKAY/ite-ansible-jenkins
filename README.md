

## Generate KEY PAIR for jenkins user 
```bash
sudo su -s /bin/bash jenkins

# Recommended (ED25519)
ssh-keygen -t ed25519 -C "jenkins_key"
# run this one for custom file name 
ssh-keygen -t ed25519 -f ~/.ssh/jenkins_key -C "jenkins"

# Alternative (RSA 4096)
ssh-keygen -t rsa -b 4096 -C "jenkins@yourdomain.com"
```