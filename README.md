# caddyscale

1. Generate an Auth key via <https://login.tailscale.com/admin/settings/keys>
1. Enable Tailscale SSH (optional) via <https://login.tailscale.com/admin/acls>
1. Enable MagicDNS (optional) via <https://login.tailscale.com/admin/dns>
1. Enable HTTPS Certificates via <https://login.tailscale.com/admin/dns>

Replace `<domain-alias>` in (e.g. `"*.<domain-alias>.ts.net"`) with your tailscale domain alias in `deploy.yaml`.

```bash
kubectl apply -f caddyscale.yaml

TS_HOSTNAME='caddyscale'
TS_DOMAIN_ALIAS='hello-world'
echo "https://${TS_HOSTNAME}.${TS_DOMAIN_ALIAS}.ts.net"
```
