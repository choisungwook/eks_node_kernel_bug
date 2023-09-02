# 개요
* eksctl로 eks cluster 생성

# 전제조건
* eksctl이 설치되어 있어야 함

# 사용방법
## 생성
```bash
eksctl create cluster -f cluster.yaml
```

## 삭제
```bash
eksctl delete cluster -f cluster.yaml
```
