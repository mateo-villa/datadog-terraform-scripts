## Terraform Scripts for Datadog Synthetic Tests

### Setup

Run the following command to export your Terraform environment variables:

```
source ./scripts/setup_env_vars.sh
```

### Troubleshooting

Permission denied when running `setup_env_vars.sh`:

Run the following command to make this script executable:

```
chmod +x setup_env_vars.sh
```

### References

(Terraform resources)[https://registry.terraform.io/providers/DataDog/datadog/latest/docs/resources/synthetics_test]
