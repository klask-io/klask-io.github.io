# helm-repo

This is a helm repository for klask

# Adding a new version or chart to this repo

```bash
$ helm package $YOUR_CHART_PATH/ # build the tgz file and copy it here
$ helm repo index . # create or update the index.yaml for repo
$ git add .
$ git commit -m 'New chart version'
```

# How to use it as a helm repo

You might know github has a raw view. So simply use the following:

```bash
$ helm repo add klask-io 'https://klask.io/charts'
$ helm repo update
$ helm search repo klask
NAME            	VERSION	DESCRIPTION
klask-io/klask	0.1.0  	A Helm chart for Klask in Kubernetes
```
