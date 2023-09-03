# 1. 개요
* EKS 커널버그를 재현

# 2. 실행방법
## 2.1 EKS 생성
* 버그가 있는 버전으로 EKS생성
```bash
cd eksctl
eksctl create cluster -f cluster.yaml
```

## 2.2 커널 파라미터 수정
* pod를 많이 생성해야 버그가 재현되는데, pod를 적제 생성하면서 버그를 재현하기 위해 커널 파라미터 수정
```bash
sysctl net.core.bpf_jit_limit=720896
```

## 2.3 pod 생성
```bash
cd manifests
kubectl apply -f deployment.yaml
```
