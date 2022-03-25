docker_build("vfarcic/devops-toolkit", ".")

k8s_yaml(kustomize("kustomize/overlays/dev"))

k8s_resource('devops-toolkit', port_forwards="8080:80")
