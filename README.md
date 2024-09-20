## Terraform Scripts for Datadog Synthetic Tests

### Setup

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

(Terraform resources)[https://registry.terraform.io/providers/DataDog/datadog/latest/docs/resources/synthetics_test]
