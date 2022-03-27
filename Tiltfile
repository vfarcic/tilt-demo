# docker_build("vfarcic/devops-toolkit", ".")

# custom_build(
#     "vfarcic/devops-toolkit",
#     "build-image.sh",
#     ["."],
#     skips_local_docker=True,
# )

load('ext://nerdctl', 'nerdctl_build')

nerdctl_build(
    ref="vfarcic/devops-toolkit",
    context=".",
)

k8s_yaml(kustomize("kustomize/overlays/dev"))

k8s_resource("devops-toolkit", port_forwards="8080:80")

local_resource(
    "tests",
    cmd="echo I was too lazy to write tests for this demo",
)
