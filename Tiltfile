# -*- mode: Python -*-

repository_name = "taurus-with-tilt"
project_name = 'samples'

docker_build(
  repository_name + '-image',
  'config',
  dockerfile='./config/Dockerfile'
)

k8s_yaml('config/kub-tilt.yaml')
k8s_resource(repository_name, labels=project_name + "-pods")
