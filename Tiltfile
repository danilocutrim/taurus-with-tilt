# -*- mode: Python -*-

repository_name = "taurus-with-tilt"
project_name = 'samples'

docker_build(
  repository_name + '-image',
  '.tilt',
  dockerfile='./.tilt/Dockerfile'
)

k8s_yaml('.tilt/kub-tilt.yaml')
k8s_resource(repository_name, labels=project_name + "-pods")
