<img width="30%" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Kubernetes_logo_without_workmark.svg/1234px-Kubernetes_logo_without_workmark.svg.png" />

# Kube(Minikube) & Docker 
(NodePort 단순 실행 / MacOS 기준)

0.
<code> & minikube start </code>

1.
<code> & eval $(minikube -p minikube docker-env) </code>

2.
<code> & kubectl run [NAME] -it --tty --image=[LocalImageName/Tag:Version] --port=[ContainerPort] </code>

(shell 빠져 나올때는 ctrl + q + p)


3.
여기의 NAME을 expose NAME 으로 사용

<code> & kubectl get pods </code>


4.
<code> & kubectl expose pod [NAME] --port=[ContainerPort] --name=[NAME] --type=NodePort </code>


5.
PORT들 확인

<code> & kubectl get svc </code>


6.
클러스터 확인

<code> & kubectl cluster-info </code>

7.
<code> & minikube dashboard </code>

WEB 접속 또는 Curl 등 HTTP 통신으로 테스트 가능
