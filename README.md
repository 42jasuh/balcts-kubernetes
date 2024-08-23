# balcts-kubernetes

`balcts-kubernetes`는 Kubernetes 환경에서 `balcts` 애플리케이션을 배포하기 위한 *.yaml 파일 모음집입니다. 이 프로젝트를 로컬에서 실행하기 사용한 모든 소프트웨어, 그리고 아키텍처 구성에 대해 작성하였습니다.

## 아키텍처 구성도
  
![image](https://github.com/user-attachments/assets/c0d978c5-aae9-4ef1-a1c8-4181fea600fd)

## 필수 소프트웨어

1. **Kubernetes 클러스터**
   - Google Kubernetes Engine (GKE) 사용

2. **Helm**
   - v3.15.4

3. **kubectl**
   - Client Version: v1.30.2

4. **Docker**
   - version 27.1.1

## 사용 이미지
1. **docker public registry**
   - woodstock93/api_server:1

## 실행 순서


1. **레포지토리 클론**

    ```bash
    git clone git@github.com:42jasuh/balcts-kubernetes.git
    
    cd balcts-kubernetes
    ```

2. **yaml 파일 적용**

    ```bash
    kubectl apply -f postgres-storage.yaml
    kubectl apply -f postgres-deployment.yaml
    kubectl apply -f django-storage.yaml
    kubectl apply -f django-deployment.yaml
    kubectl apply -f config.yaml
    ```
