# helm 차트 배포 방법
1. helm chart 생성
2. helm chart 패키징
```shell
helm package {chart 경로}
```
3. helm chart index.yaml 생성
```shell
helm repo index --url <github_repository_path> . --merge index.yaml
```
4. index.yaml에서 각 chart url 수정
5. git push
```shell
git add index.yaml
git commit -m "{message}"
git push
```

# helm 차트 사용방법
```shell
helm repo add my-repo https://build-deploy-pipeline.github.io/helm-charts/
helm repo update
helm search repo my-repo
```

# 참고자료
* https://www.opcito.com/blogs/creating-helm-repository-using-github-pages
