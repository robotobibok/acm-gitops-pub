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



3. deploy app 
one or more objects failed to apply, reason: deployments.apps is forbidden: User "system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller" cannot create resource "deployments" in API group "apps" in the namespace "nginx-sample",routes.route.openshift.io is forbidden: User "system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller" cannot create resource "routes" in API group "route.openshift.io" in the namespace "nginx-sample",services is forbidden: User "system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller" cannot create resource "services" in API group "" in the namespace "nginx-sample" (retried 5 times).

https://github.com/redhat-developer/gitops-operator/blob/master/docs/OpenShift%20GitOps%20Usage%20Guide.md#deploy-resources-to-a-different-namespace

