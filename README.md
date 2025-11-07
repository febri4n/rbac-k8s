Penggunaan di teleport
```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: cluster-admin-to-user-febri4n # Nama ClusterRole yang akan di assign
subjects:
  - kind: User
    name: febri4n # Nama User di teleport
    apiGroup: rbac.authorization.k8s.io
roleRef:
  kind: ClusterRole
  name: cluster-admin # ClusterRole lainnya: admin,view,edit 
  apiGroup: rbac.authorization.k8s.io
```
Apply di cluster
```bash
kubectl apply -f rbac.yaml
```
