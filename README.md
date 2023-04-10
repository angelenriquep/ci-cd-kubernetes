# Go - Kubernets - CI/CD example

go run blog.go main.go  

## Ensure jenkins image has the lastest tools

apt-get install build-essential
docker ps && docker exec -it --user root 3c685e2e273b /bin/bash

## Jenkings password generation

Once we have run Jenkins we have to excute above to get the admin password:

```sh
dc up -d
docker exec jenkins-lts cat /var/jenkins_home/secrets/initialAdminPassword
docker logs jenkins | less
```
