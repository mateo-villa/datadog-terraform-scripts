## Terraform Scripts for Datadog Synthetic Tests

### Setup

Rename the `./scripts/setup_env_vars.sh.example` file to `./scripts/setup_env_vars.sh`. In this file, input your Datadog API and Application keys:

```
export TF_VAR_datadog_api_key="<Your-API-Key>"
export TF_VAR_datadog_app_key="<Your-App-Key>"
```

If your org is in US1, you can delete the rest of the file. Otherwise, make sure your site is set to the correct region (e.g. US5):

```
export TF_VAR_datadog_site="us5.datadoghq.com"
export TF_VAR_datadog_api_url="https://api.us5.datadoghq.com"
```

Run the following command to export your Terraform environment variables:

```
source ./scripts/setup_env_vars.sh
```

### Apply your Synthetic Test configuration

Run the following commands to initialize Terraform:

```
terraform init
```

Run the following commands to apply your configuration:

```
terraform apply
```

You should now see your tests show up in the Datadog UI!

### Troubleshooting

Permission denied when running `setup_env_vars.sh`:

Run the following command to make this script executable:

```
chmod +x ./scripts/setup_env_vars.sh
```

### References

[Terraform resources](https://registry.terraform.io/providers/DataDog/datadog/latest/docs/resources/synthetics_test)
