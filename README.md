## What is this?
This repository contains examples of stuff I run in k3s at home. You can take a look at [this repo](https://github.com/panoptikoe/k3s-ansible) which is based on [this one](https://github.com/timothystewart6/k3s-ansible) to learn more about how I deploy k3s. 

In short, i have two proxmox nodes where I run a lot of VMs on, an OPNSense firewall, three Raspberry Pi's (which run [Pimox 7](https://github.com/pimox/pimox7), and have some VMs on them part of the k3s cluster) and a Mikrotik switch. And yes, three Unifi access points, so I need that Unifi-controller.

Feel free to use these examples if it is in any way useful to you. I'm by no means an expert and have hacked my way through this, after work and in weekends / vacations. Any questions can be posed by opening an issue or contacting me through GitHub; I'll try to get back to them.

## Thank you
To the following repositories / people:
- https://github.com/pimox/pimox7
- https://github.com/timothystewart6/k3s-ansible (I wouldn't have even tried to do something with Kubernetes without it)
- The makers of a shitload of opensource software I use regularly (OPNSense, Traefik, Proxmox, Linux, ... the list goes on and on)
