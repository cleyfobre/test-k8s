## minikub에 적용하기

### config와 secret 생성
```agsl
kubectl apply -f mongo-config.yml
kubectl apply -f mongo-secret.yml
```

### deployment 생성
```agsl
kubectl apply -f mongo.yml
kubectl apply -f webapp.yml
```

### 생성된 컴포넌트들 확인
```agsl
kubectl get all
kubectl get configmap
kubectl get secret
kubectl get pod
```

### 컴포넌트 상세 확인
```agsl
kubectl --help
kubectl get --help
kubectl describe service webapp-service
kubectl describe pod webapp-deployment-54957cb9dc-k8kqp
```

### 컴포넌트 디버깅
```agsl
kubectl logs webapp-deployment-54957cb9dc-k8kqp
kubectl logs webapp-deployment-54957cb9dc-k8kqp -f
```

### 브라우져에서 확인
- 서비스에서 포트 확인
```agsl
kubectl get service
```
- minikube ip 확인
- 아래 두 명령어의 결과에 같은 ip가 표시됨을 확인
```agsl
minikube ip
kubectl get node -o wide
```
