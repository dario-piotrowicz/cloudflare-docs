---
_build:
  publishResources: false
  render: never
  list: never
---

- Run a [`cloudflared` replica](/cloudflare-one/connections/connect-networks/deploy-tunnels/deploy-cloudflared-replicas/#cloudflared-replicas) on two dedicated host machines per network location. Using two hosts enables server-side redundancy and traffic balancing.
- Size each host with minimum 4GB of RAM and 4 CPU cores.
- Allocate 50,000 [ports](#number-of-ports) to the `cloudflared` process on each host.

This setup is usually sufficient to handle traffic from 8,000 users (4,000 per host).