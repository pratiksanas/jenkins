## 1. Create an EC2 instance for Agent & Install :
SSH >>
```
sudo apt update
sudo apt install fontconfig openjdk-21-jre
java -version
```
## 2. Create a public key & private key on Jenkins master :
SSH >>
```
cd ~/.ssh
ssh-keygen
```
## 3. Add a new Agent :
Jenkins >> Nodes >> New Nodes
- Node Name : agent-pratik
- type : permanent agent
- labels : pratik
- Remote root directory : /home/ubuntu
- Launch method : launch agent via ssh
  - add host : <agent ip>
  - private key : <add the private key in credentials from master from step 2>
- host key verification strategy : non verifying verification startegy.

## 4. Add public key on agent's instance :
- Go to ~/.ssh >> authorized_keys >> add the public key (Refer step 2)

## 5. Click on launch agent
