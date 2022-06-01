# Deploy WordPress Instance on Kubernetes

### 1. Clone the repository
    $ git https://github.com/paawanyadav/kubernetes_wordpress-mysql.git
    $ cd wordpress

### 2. Configure password for DB or leave it default 
    => Before make changes in mysql-secret.yaml encode your values
    $ For Encode --> echo -n "Yourvalue" | base64
    $ For Decode --> echo -n "EncodedValue" | base64 -d
    $ nano mysql-secret.yaml

### 3. Apply files 
    $ kubectl apply -f mysql-secret.yaml
    $ kubectl apply -f mysql.yaml
    $ kubectl db-connection-configmap.yaml
    $ kubectl wordpress.yaml

### 5. By Using NodePort
    -- Uncomment line 56 and 63
    -- Again Follow Apply files 

### 6. By Using Ingress

