# Test

#cat << EOF | kubectl --context $PLATFORM apply -f -
#---
#apiVersion: v1
#kind: Secret
#metadata:
#  name: gitlab-credentials
#  namespace: default
#type: Opaque
#data:
#  username: $username_base64
#  password: $PAT_base64
#---
#apiVersion: platform.kratix.io/v1alpha1
#kind: GitStateStore
#metadata:
#  name: default
#  namespace: default
#spec:
#  path: $dir
#  branch: main
#  secretRef:
#    name: gitlab-credentials
#    namespace: default
  url: https://gitlab-url
EOF
