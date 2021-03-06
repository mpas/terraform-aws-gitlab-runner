# Example - Runner - Docker runner

Example how create a gitlab runner using the docker executor on a single node, running in a private subnet.

## Prerequisite

The terraform version is managed using [tfenv](https://github.com/Zordrak/tfenv). If you are not using `tfenv` please check `.terraform-version` for the tested version.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| aws\_region | AWS region. | string | `"eu-west-1"` | no |
| environment | A name that identifies the environment, will used as prefix and for tagging. | string | `"runners-docker"` | no |
| gitlab\_url | URL of the gitlab instance to connect to. | string | `"https://www.gitlab.com"` | no |
| private\_ssh\_key\_filename |  | string | `"generated/id_rsa"` | no |
| public\_ssh\_key\_filename |  | string | `"generated/id_rsa.pub"` | no |
| registration\_token |  | string | n/a | yes |
| runner\_name | Name of the runner, will be used in the runner config.toml | string | `"docker"` | no |
