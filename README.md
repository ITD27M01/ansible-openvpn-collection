# Ansible Roles for OpenVPN setup (Oracle Cloud Infrastructure)

Three roles intended to setup OpenVPN server for internal cloud resources access.

* `openvpn` role configures openvpn server
* `iptables` role configures NAT and firewall rules
* `unbound` role configures DNS resolution for VPN clients

## Installing collection from Ansible Galaxy

```
$ ansible-galaxy collection install itd27m01.oci_openvpn
```

## Variables

`openvpn` role uses OCI Vault for certificates setup as a storage of certs and
private keys. Special lookup plugin available in `itd27m01.oci` collection and
used for pki data retrieving.

So, three variables are required for OCI Vault access:

```yaml
secret_compartment_id: 'ocid1.tenancy.oc1..someidentity'
secret_vault_id: 'ocid1.vault.region.vault_namespace.someid'
secret_key_id: 'ocid1.key.oc1.region.vault_namespace.some_another_id'
```

## Authentication
Authentication as well as dynamic inventory assume the presents of `OCI_CONFIG_PROFILE` environment variable.
