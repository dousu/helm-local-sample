# List Releases

```
helm list -n mysql-ns
```

# Manifests

```sh
helm template mysql-sample stable/mysql -n mysql-ns --values helm/values/mysql/values.yaml --output-dir helm/values/mysql
```

# Install

```sh
// When the namespace has not created yet
kubectl create ns mysql-ns

helm install mysql-sample stable/mysql -n mysql-ns --values helm/values/mysql/values.yaml
```

# Upgrade

```sh
// When the namespace has not created yet
kubectl create ns mysql-ns

helm install mysql-sample stable/mysql -n mysql-ns --values helm/values/mysql/values.yaml
```

# Status of Release

```sh
helm status mysql-sample
```

# Test

Use thi DNS name `mysql-sample.mysql-ns.svc` .

```sh
helm test mysql-sample -n mysql-ns
```
