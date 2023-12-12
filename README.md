# Versions

This repository contains a collection of metadata that is used to capture information about Wolfi package versions.

An example YAML file:

```yaml
apiVersion: versions.wolfi.dev/v1 # versioned schema
kind: VersionStream
metadata:
  name: golang
spec:
  backend: end_of_life # backend used to update version status data below
  backend_uri: https://endoflife.date # uri to use when fetching version data
  identifier: go # identifier to lookup matching version data in backend service
  versionStreamFormat: ${{name}}-${{versions.major}}.${{versions.minor}} # pattern used to map wolfi version stream packages
status:
  eolVersions:
    - eolDate: "2023-08-08"
      releaseDate: "2022-08-02"
      version: "1.19"
    - eolDate: "2023-02-01"
      releaseDate: "2022-03-15"
      version: "1.18"
    - eolDate: "2022-08-02"
      releaseDate: "2021-08-16"
      version: "1.17"
    - eolDate: "2022-03-15"
      releaseDate: "2021-02-16"
      version: "1.16"
    - eolDate: "2021-08-16"
      releaseDate: "2020-08-11"
      version: "1.15"
    - eolDate: "2021-02-16"
      releaseDate: "2020-02-25"
      version: "1.14"
    - eolDate: "2020-08-11"
      releaseDate: "2019-09-03"
      version: "1.13"
    - eolDate: "2020-02-25"
      releaseDate: "2019-02-25"
      version: "1.12"
    - eolDate: "2019-09-03"
      releaseDate: "2018-08-24"
      version: "1.11"
    - eolDate: "2019-02-25"
      releaseDate: "2018-02-16"
      version: "1.10"
  latestVersion: 1.21.4
  versions:
    - releaseDate: "2023-08-08"
      version: "1.21"
    - releaseDate: "2023-02-01"
      version: "1.20"
```