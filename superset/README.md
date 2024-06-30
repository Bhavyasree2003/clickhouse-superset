## superset deploymen into minikube

* to intall __superset__ run the below commands
* we are using helm __to immplent simple and best way__
```
helm repo add superset https://apache.github.io/superset
helm upgrade --install --values custom-values.yaml superset superset/superset
```

*  the below are the reasons , to consider __custome-values.yaml__ file to install helm chat
* expose __superset__  to __NodePort__
* to change  the default __SECRET_KEY__ to custom value

## the below commands we need to documentntation

* helm repo add superset https://apache.github.io/superset


``` 
we will reciece the below erro deu to that we need customixe
--------------------------------------------------------------------------------
A Default SECRET_KEY was detected, please use superset_config.py to override it.
Use a strong complex alphanumeric string and use a tool to help you generate
a sufficiently random sequence, ex: openssl rand -base64 42
--------------------------------------------------------------------------------
--------------------------------------------------------------------------------
Refusing to start due to insecure SECRET_KEY
[2024-06-30 13:00:07 +0000] [99] [INFO] Worker exiting (pid: 99)
Loaded your LOCAL configuration at [/app/pythonpath/superset_config.py]

```


* for thart we need to run __openssl rand -base64 42__

```
configOverrides:
  secret: |
    SECRET_KEY = 'YOUR_OWN_RANDOM_GENERATED_SECRET_KEY
```

* that values are updated in the ![file](./custom-values.yaml)

