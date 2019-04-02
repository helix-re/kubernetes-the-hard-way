# Installing the Client Tools

In this lab you will install the command line utilities required to complete this tutorial: [cfssl](https://github.com/cloudflare/cfssl), [cfssljson](https://github.com/cloudflare/cfssl), and [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl).


## Install CFSSL

The `cfssl` and `cfssljson` command line utilities will be used to provision a [PKI Infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure) and generate TLS certificates.

```
brew install cfssl
```

### Verification

Verify `cfssl` version 1.2.0 or higher is installed:

```
cfssl version
```

> output

```
Version: 1.2.0
Revision: dev
Runtime: go1.6
```

Verify `cfssljson` version 1.2.0 or higher is installed:

```
cfssl -version
```

> output

```
Version: 1.2.0
Revision: dev
Runtime: go1.6
```

## Install kubectl

The `kubectl` command line utility is used to interact with the Kubernetes API Server. Download and install `kubectl` from the official release binaries:

```
curl -o kubectl https://storage.googleapis.com/kubernetes-release/release/v1.12.0/bin/darwin/amd64/kubectl
```

```
chmod +x kubectl
```

```
sudo mv kubectl /usr/local/bin/
```


### Verification

Verify `kubectl` version 1.12.0 or higher is installed:

```
kubectl version --client
```

> output

```
Client Version: version.Info {Major:"1", Minor:"12", GitVersion:"v1.12.0",
GitCommit:"0ed33881dc4355495f623c6f22e7dd0b7632b7c0", GitTreeState:"clean",
BuildDate:"2018-09-27T17:05:32Z", GoVersion:"go1.10.4", Compiler:"gc", Platform:"linux/amd64"}
```

Next: [Provisioning Compute Resources](03-compute-resources.md)
