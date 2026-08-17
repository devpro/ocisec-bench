# Sysdig

[Sysdig Secure Onboarding Pipeline Scanning](https://docs.sysdig.com/en/sysdig-secure/install-vulnerability-cli-scanner/)

```bash
SYSDIG_CLI_SCANNER_VERSION=$SYSDIG_CLI_SCANNER_VERSION
curl -LO "https://download.sysdig.com/scanning/bin/sysdig-cli-scanner/${SYSDIG_CLI_SCANNER_VERSION}/linux/amd64/sysdig-cli-scanner"
sha256sum -c <(curl -sL "https://download.sysdig.com/scanning/bin/sysdig-cli-scanner/${SYSDIG_CLI_SCANNER_VERSION}/linux/amd64/sysdig-cli-scanner.sha256")
chmod +x ./sysdig-cli-scanner
```
