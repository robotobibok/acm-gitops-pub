# acm-gitops-pub


1. Uprawnienia 
```bash
cat > crb-patch.yaml << EOF
subjects:
- apiGroup: rbac.authorization.k8s.io
  kind: User
  name: kube:admin
EOF
  ```

``oc patch clusterrolebinding open-cluster-management:subscription-admin --patch-file ./crb-patch.yaml``

2. Tagowanie klastrow