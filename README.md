# rd-fluxcd-lesson

Boostrap
```
GITHUB_TOKEN=$(gh auth token) flux bootstrap github \
--owner=kyrylich \
--repository=rd-fluxcd-lesson \
--branch=main \
--path=./clusters/my-cluster \
--personal
```

Debug
```
k kustomize overlays/development
k kustomize overlays/production

flux get kustomizations
```

```
flux create secret tls course-app-tls \
--namespace=development \
--tls-crt-file=./course-app.pem \
--tls-key-file=./course-app-key.pem

flux create secret tls course-app-tls \
--namespace=production \
--tls-crt-file=./course-app.pem \
--tls-key-file=./course-app-key.pem 
```
