# Helm Chart Examples

The following repository contains examples of using Helm Charts to accomplish specific operations

## Config Files in a Secret

The __file-secrets.yaml__ template contains examples for embedding external configuration files as base-64 entries.  The value from test-file.json is configured for applying information from a values file into the content of the file.

Along with this file is the ability to inject an external file for the handle bars template file in the secret.  This is done by using the command option `--set-file hbcontent=./template.hbs`.  The full command to install this chart would be:

```bash
helm install example-app examples/example-charts -f .\values.yaml --set-file hbcontent=./template.hbs
```

