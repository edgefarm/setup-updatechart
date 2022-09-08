# setup-updatechart
Update helm chart dependencies that are managed within the same repository and own version

**Usage**

```sh
- uses: edgefarm/setup-updatechart@v1.1.0
- run: updateChart <args>
```


**Options**

```sh
$ updateChart --help
    -h, --help               Display this help
    -c, --chart              Chart.yaml to update
    -v, --new-version        New version to set for the chart and its dependencies
    -k, --keep-version       Keep the old version of the chart. Only sets dependencies versions.
    -l, --local-charts-dir   Location where local managed dependency charts are located
    -r, --repository         Repository of the chart
```

**Example**

```sh
    updateChart --chart charts/core/Chart.yaml --new-version 2.3.4 --local-charts-dir charts --repository oci://ghcr.io/edgefarm/edgefarm.core
```
