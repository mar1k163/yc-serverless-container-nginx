# yc-serverless-container-nginx

### To get started, you will need:

- Create a service account: https://yandex.cloud/ru/docs/iam/operations/sa/create
- Assign a role to a service account: https://yandex.cloud/ru/docs/iam/operations/sa/assign-role-for-sa
- Create a registry: https://yandex.cloud/ru/docs/container-registry/operations/registry/registry-create
- Authenticate to CR: https://yandex.cloud/ru/docs/container-registry/operations/authentication

### Container Assembly:
```
docker build . -t cr.yandex/<id_registry>/nginx:latest
```
### Push the container to the Container Registry:
```
docker push cr.yandex/<id_registry>/nginx:latest
```
### Create a container:

https://yandex.cloud/ru/docs/serverless-containers/operations/create

### Create a container revision: 

https://yandex.cloud/ru/docs/serverless-containers/operations/manage-revision

### Calling the container:

https://yandex.cloud/ru/docs/serverless-containers/operations/invoke

### Result:

```
curl https://<id_container>.containers.yandexcloud.net/              
```
```
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>

```

