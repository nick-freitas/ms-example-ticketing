# Microservices Example Project (Ticketing)

## Services
[ms-example-ticketing.auth](https://github.com/nick-freitas/ms-example-ticketing.auth)

[ms-example-ticketing.mset-client](https://github.com/nick-freitas/ms-example-ticketing.mset-client)


## Dev Notes

* AFTER CLUSTER PURGE, YOU NEED TO RUN:

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.48.1/deploy/static/provider/cloud/deploy.yaml
```

* Clone and Run

``` bash
git clone https://github.com/nick-freitas/ms-example-ticketing.git
cd ms-example-ticketing/auth
git clone https://github.com/nick-freitas/ms-example-ticketing-auth.git .
cd ../../
cp skaffold.exe .\ms-example-ticketing\
cd .\ms-example-ticketing\
./skaffold.exe dev
```

* JWT Secret Key

```
kubectl create secret generic jwt-secret --from-literal=JWT_SECRET_KEY=FAKE_SECRET_KEY
``` 
