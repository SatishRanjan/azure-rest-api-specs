## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go) && !$(track2)
go:
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: web
  clear-output-folder: true
```

```yaml $(go) && $(track2)
license-header: MICROSOFT_MIT_NO_VERSION
module-name: sdk/resourcemanager/appservice/armappservice
module: github.com/Azure/azure-sdk-for-go/$(module-name)
output-folder: $(go-sdk-folder)/$(module-name)
azure-arm: true
directive: 
- rename-model: 
    from: 'AppServiceCertificate'
    to: 'CertificateModel'
- rename-model:
    from: 'AppServiceCertificateCollection'
    to: 'CertificateCollectionModel'
- rename-model:
    from: 'AppServiceCertificatePatchResource'
    to: 'CertificatePatchResourceModel'
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2021-03
  - tag: package-2021-02
  - tag: package-2021-01-15
  - tag: package-2020-12
  - tag: package-2020-09
  - tag: package-2020-06
  - tag: package-2019-08
  - tag: package-2018-02
  - tag: package-2016-09
  - tag: package-2015-08-preview
```

### Tag: package-2021-03 and go

These settings apply only when `--tag=package-2021-03 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-03' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2021-03-01/$(namespace)
```

### Tag: package-2021-02 and go

These settings apply only when `--tag=package-2021-02 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-02' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2021-02-01/$(namespace)
```

### Tag: package-2021-01-15 and go

These settings apply only when `--tag=package-2021-01-15 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-01-15' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2021-01-15/$(namespace)
```

### Tag: package-2020-12 and go

These settings apply only when `--tag=package-2020-12 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2020-12' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2020-12-01/$(namespace)
```

### Tag: package-2020-09 and go

These settings apply only when `--tag=package-2020-09 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2020-09' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2020-09-01/$(namespace)
```

### Tag: package-2020-06 and go

These settings apply only when `--tag=package-2020-06 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2020-06' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2020-06-01/$(namespace)
```

### Tag: package-2019-08 and go

These settings apply only when `--tag=package-2019-08 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2019-08' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2019-08-01/$(namespace)
```

### Tag: package-2018-02 and go

These settings apply only when `--tag=package-2018-02 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2018-02' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2018-02-01/$(namespace)
```

### Tag: package-2016-09 and go

These settings apply only when `--tag=package-2016-09 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2016-09' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2016-09-01/$(namespace)
```

### Tag: package-2015-08-preview and go

These settings apply only when `--tag=package-2015-08-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2015-08-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2015-08-01-preview/$(namespace)
```
