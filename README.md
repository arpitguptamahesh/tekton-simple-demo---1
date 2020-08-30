# Project Overview

A basic demo to run a simple example of tekton pipelone

## Pre-requisites

- Docker: https://docs.docker.com/engine/install/
- Kubernetes: https://kubernetes.io/es/docs/tasks/tools/install-kubectl/
- Tekton: https://tekton.dev/docs/getting-started/#installation

# Running

## Create the Resources for Task and Pipeline

```sh
kubectl apply -f task.yaml
kubectl apply -f pipeline.yaml
```

# Running just the Task

To run a `Task` is necessary to create a `TaskRun` resource which runs the `Task`

```sh
kubectl create -f task-run.yaml
```

# Running the Pipeline

To run a `Pipeline` is necessary to create a `PipelineRun` resource which runs the `Pipeline`.
If your `Pipeline` use some resources like a repository or docker images, you nee to create a
`PipelineResource`.

```sh
kubectl create -f pipeline-run.yaml
```

**Tekton documentation:** https://tekton.dev/
