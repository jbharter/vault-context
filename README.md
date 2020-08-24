# vault-context
vault-context is a context manager and token helper designed to make
managing multiple vaults easier

```
vault-context is a context manager and token helper designed to make
managing multiple vaults easier

Usage:
  vault-context [command]

Available Commands:
  add         Add a new Vault context
  context     Spawn a shell in the given context
  delete      Delete a saved context
  enable      Set vault-context as the token-helper
  help        Help about any command
  info        Get info about your current context
  list        List configured contexts

Flags:
  -h, --help   help for vault-context

Use "vault-context [command] --help" for more information about a command.
```

## Examples:
```
vault-context list
 ALIAS     URL                            NAMESPACE                  TOKEN                      
 home      https://vault.domain.tld                                  s.7asdfrYasdf 
 cloud     https://vault.aws.domain.tld                              -                          
 test      https://test.vault.domain.tld  eadp-techops-cloud-devops  -     
```

## Quickstart
1. Download the [latest release](https://github.com/itscontained/vault-context/releases)
2. Add it to your `/usr/local/bin` and make it executable
3. Enable using it as your token-manager `vault-context enable`
4. Add your first context `vault-context add http://vault.domain.tld my-vault`
5. Assume the context `vault-context context my-vault`
```