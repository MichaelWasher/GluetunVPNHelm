# Gluetun VPN Helm
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/gluetun-vpn)](https://artifacthub.io/packages/search?repo=gluetun-vpn)

Gluetun VPN Helm is a HelmChart that is used to install and configure the [Gluetun VPN Client tool](https://github.com/qdm12/gluetun).

Gluetun is a lightweight swiss-knife-like VPN client that is used to connect to multiple VPN service providers.

Supported Providers: Cyberghost, ExpressVPN, FastestVPN, HideMyAss, IPVanish, IVPN, Mullvad, NordVPN, Perfect Privacy, Privado, Private Internet Access, PrivateVPN, ProtonVPN, PureVPN, Surfshark, TorGuard, VPNUnlimited, Vyprvpn, WeVPN, Windscribe servers

For more information about Gluetun, refer to the [Gluetun GitHub Page](https://github.com/qdm12/gluetun) or the [Gluetun Wiki](https://github.com/qdm12/gluetun/wiki).

## Additional Notes:
This HelmChart was created to split separate the complexities of VPN configuration outside of my Kubernetes environment using Cyberghost.

This currently has only been tested using CyberGhost using OpenVPN configuration, but as this tool is only performing configuration the testing does not need to be as extensive.

I will gradually be adding additional options into the `Values.yml` configuration file to meet my customisation needs but PRs are WELCOME, especially those that will provide the ability to test / use additional VPN providers.

## Setting up Helm Chart

Set the following `values` with those provided by a supported VPN Provider and install the HelmChart.
```yaml
# --- Custom Config
client:
  user: "USER"
  password: "PASS"
  certificate: |
    -----BEGIN CERTIFICATE-----
    ...........................
    -----END CERTIFICATE-----
  ca: |
    -----BEGIN CERTIFICATE-----
    ...........................
    -----END CERTIFICATE-----
  key: EXAMPLEKEY
  country: Australia
  vpnProvider: Cyberghost
```
