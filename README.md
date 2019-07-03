# dockercicd
End-to-End Prototype for Jenkins to build Docker images within a docker jenkins container

A Jenkins Docker image with plugins to build docker images

```
sudo useradd -u 1000 jenkins
sudo rm -rf /opt/cicd/jenkins
sudo mkdir /opt/cicd/jenkins
sudo chown -R jenkins:jenkins /opt/cicd/jenkins
```

chown 1000
sudo rm -rf /opt/cicd/jenkins
sudo mkdir /opt/cicd/jenkins
sudo chown 1000 /opt/cicd/jenkins
docker run -it -p 8080:8080 --name jenkins -v /opt/cicd/jenkins:/var/jenkins_home:z jenkins/jenkins:2.183

"Volumes": {
	"/var/jenkins_home": {}
},
 
"Env": [
	"PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
	"LANG=C.UTF-8",
	"JAVA_HOME=/usr/local/openjdk-8",
	"JAVA_VERSION=8u212-b04",	"JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u212-b04/OpenJDK8U-",
	"JAVA_URL_VERSION=8u212b04",
	"JENKINS_HOME=/var/jenkins_home",
	"JENKINS_SLAVE_AGENT_PORT=50000",
	"JENKINS_VERSION=2.183",
	"JENKINS_UC=https://updates.jenkins.io",
	"JENKINS_UC_EXPERIMENTAL=https://updates.jenkins.io/experimental",
	"JENKINS_INCREMENTALS_REPO_MIRROR=https://repo.jenkins-ci.org/incrementals",
	"COPY_REFERENCE_FILE_LOG=/var/jenkins_home/copy_reference_file.log"




