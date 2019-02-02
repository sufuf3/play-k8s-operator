# play-k8s-operator

Play with [operator-sdk](https://github.com/operator-framework/operator-sdk) to generate a Helm-based operator.

## Setup the Project play-k8s-operator Flow

Please refer to: https://github.com/operator-framework/operator-sdk

### 1. Create a vagrant & setup Kubernetes

- OS: Centos

```sh
cd vagrant/ && vagrant up
vageant ssh
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

### 2. Install the operator-sdk CLI

Ref: https://github.com/operator-framework/operator-sdk#quick-start

```sh
go get -u github.com/golang/dep/cmd/dep
go get -u github.com/operator-framework/operator-sdk
cd ~/go/src/github.com/operator-framework/operator-sdk
make dep
make install
```

### 3. Create a Helm-based operator project using the SDK CLI

```sh
mkdir -p $GOPATH/src/github.com/<GitHub_ID>
cd $GOPATH/src/github.com/<GitHub_ID>
operator-sdk new play-k8s-operator --api-version=samina.fu.com/v1alpha1 --kind=MyTest --type helm          # operator-sdk new <project-name> --type=helm --kind=<kind> --api-version=<group/version>
cd play-k8s-operator/
```
