# AKS Probes

POC to add a set of in-cluster probes that reflect health through readiness check.

## Environment

* `TARGET_HOSTNAME`: hostname to test
* `TARGET_PORT`: port to probe
* `TARGET_TIMEOUT`: TCP timeout when probing port

## Current Checks

* DNS resolution for `TARGET_HOSTNAME`
* TCP connectivity to `TARGET_HOSTNAME` on `TARGET_PORT`

## Usage

1. Edit `aks-probes.yaml` and update `TARGET_HOSTNAME`
2. `kubectl apply -f aks-probes.yaml`
3. Monitor the readiness probe

## Changelog

### v0.1.0

DNS and tunnel gateway connectivity checks.
