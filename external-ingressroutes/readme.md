This folder contains examples of how you can use Traefik as a reverse proxy with external-ingressroutes to get HTTPS on Web UIs like HomeAssistant, Mikrotik or Proxmox. I'm pretty sure it can be done more efficiently or different, but this "works" so I just keep using these configurations.

This obviously needs a working Traefik deployment and a working Cert-manager deployment. I followed this guide: https://technotim.com/posts/kube-traefik-cert-manager-le/ to do that.
