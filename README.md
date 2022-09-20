# kube-jenkins-dockerhub
Kubernetes yaml configuration files for Jenkins using docker hub image


This configuration has been tested on "rancher desktop"
- kubernetes <= 1.24.4
- build-in traefik disabled
- ingress traefik (v2.8) installed via "kube-traefik-ingress-controller" code repository
- no https configured


This configuration use:
- nginx v1.23.1-alpine
- jenkins v2.361.1-lts-jdk11


You need to add an entry in /etc/hosts to make working the ingress properly with "rancher desktop":
- jenkins.kube.local 127.0.0.1


You need to set a right path in /jenkins/jenkins-PersistentVolume :
- path: "/<path>/GitHub/kube-jenkins-dockerhub/volume/"


No jenkins agent installed to run build
