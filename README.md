# Infra

CLI to quickly deploy and manage your infrastructure.

## Getting Started

Make sure you have at least Go 1.19 and run:

```bash
go install .
```

## Features and Workflows

```
source env.sh && go run main.go -c aws -i t2.large -s ./scripts/run.sh -v ./scripts/verify.sh
```

- `env.sh` should be a file with all of your environment variables.

1. Starts the an `aws` `t2.large` instance.
2. Runs the script `./scripts/run.sh` when the instance started.
3. Script to verify that the instance properly started.
   1. Typically just send a request to ensure that the server properly started.
