#### Experiments with Artifactor OSS in k3s

https://www.jfrog.com/confluence/display/JFROG/Installing+Artifactory#InstallingArtifactory-DockerInstallation

Assuming you already installed the Token in your local config:

    $ export KUBECONFIG=~/.kube/config
    $ kubectl get nodes
    $ source <(kubectl completion bash)

Deploy to Kubernetes

    $ kubectl create namespace hello-artifactory
    $ kubectl config set-context --current --namespace=hello-artifactory
    $ kubectl apply -k k3s/

Then visit the [URL](https://artifactory.localhost).  Access
Artifactory from your browser at
[WebUI](http://artifactory.localhost/ui) -- default credential for
Artifactory: admin/password as user/password.

The RPM Feature is disabled in OSS Version, sigh.
