# demo-agro
Create a Helm Chart to deploy the image from the previous step. The chart should support
- Simple deployment (Deployment, Service, Ingress, etc)
- Argo Rollout resources (https://argo-rollouts.readthedocs.io/en/stable) to perform
Canary Deployment and BlueGreen Deployment
The chart should also have flexibility to allow Developers to adjust Values. They can choose to use either simple deployment or Canary or Blue Green without having to rebuild the chart frequently

## Usage - Helm

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add apichaya-s https://apichaya-s.github.io/demo-argo

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
apichaya-s` to see the charts.

To install the rollout-chart chart:

    helm install my-rollout-chart apichaya-s/rollout-chart

To uninstall the chart:

    helm delete my-rollout-chart

