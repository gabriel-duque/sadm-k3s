# sadm

This repository holds the [Helm](https://helm.sh) charts I used to deploy my
personal infrastructure.

Although you can use any Kubernetes cluster, my services run on top of
[k3s](https://k3s.io).

Here is a list of services you can find in the different folders of this
repository:

* ditto: a [Traefik](https://traefik.io/) load balancer chart with a dashboard exposed behind
  BasicAuth authentication
* lapras: a file sharing service using
  [transfer.sh](https://github.com/dutchcoders/transfer.sh) allowing
  non-authenticated downloads but enforcing BasicAuth authentication for
  uploads
* omanyte: a [chartmuseum](https://github.com/helm/chartmuseum) Helm chart
  repository with BasicAuth authentication for API endpoints
* zorua: a [homemade](https://github.com/zuh0/zorua) dynamic DNS client for
  Google Domains used as a Kubernetes cron job to keep A records up to date

For each of these charts, you can take a look at the `values.yaml` file inside
them and edit it to fit your needs.
