# Red Multi-Vendor OSPFv3 (MikroTik, VyOS, Juniper, Alpine)

## Topología e IPs Clave
- **MikroTik CHR (Backbone):** `2021:16:17:1::/64` y `2::/64`
- **Angola (Alpine + FRR):** `3::/64` (IPs: `3::1` y `3::2` en `eth2`)
- **Argentina (VyOS):** `4::/64` (IPs: `4::1` y `4::2`)
- **Australia (Juniper JunOS):** `5::/64` (IPs: `5::1` y `5::2` en `ge-0/0/2`)

## Comandos Clave
- **Linux / Alpine (Forwarding):** `sysctl -w net.ipv6.conf.all.forwarding=1`
- **FRR (`vtysh`):** `show ipv6 route`, `router ospfv3`
- **VyOS:** `set interfaces ethernet ... address ...`
- **Juniper:** `set interfaces ge-0/0/2 unit 0 family inet6 address ...`
