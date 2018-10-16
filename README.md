# Kubectl-import

`kubectl-import` is a tool for importing and merging `kubectl` configuration files.

The imported files can be raw configuration files or base64-encoded versions of those files. Base64 is helpful for sharing using tools that impose maximum line size.

## Using

```console

$ kubectl-import ~/Downloads/cluster-kubectl-config
```

The specified file(s) are merged back to your kubectl config file - `~/.kube/config` by default, unless `KUBECONFIG` environment variable is set.

In order to write output to a different file, simply set `KUBECONFIG` variable - such as:

```console

$ KUBECONFIG=/tmp/kubectl-merged kubectl-import ~/.kube/config ~/Downloads/cluster-kubectl-config
```
