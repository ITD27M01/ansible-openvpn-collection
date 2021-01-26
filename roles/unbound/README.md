# Ansible unbound role for OpenVPN server

Installs and configures unbound DNS server on OpenVPN server. It allows access to
cloud fqdns for OpenVPN users.

## Variables

Relies on `ovpn_*` variables from `openvpn` role to configure access permissions.
