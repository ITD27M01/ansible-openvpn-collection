# Ansible openvpn role for OpenVPN server

Installs and configures OpenVPN server

## Variables

Most variables are defaulted and you can use them as is. It also uses OCI Vault for certificates setup as a storage of certs and
private keys. Special lookup plugin available in `itd27m01.oci` collection and
used for pki data retrieving.

So, three variables are required for OCI Vault access:

```yaml
secret_compartment_id: 'ocid1.tenancy.oc1..someidentity'
secret_vault_id: 'ocid1.vault.region.vault_namespace.someid'
secret_key_id: 'ocid1.key.oc1.region.vault_namespace.some_another_id'
```