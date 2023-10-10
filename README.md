# Medium-Sized Business Network Design

This is another sample of academic work. The project involves the design of a comprehensive network for a medium-sized business with three sites (Site A, Site B, and Site C). The network comprises multiple rooms and hosts, interconnected through routers, switches, and firewalls, ensuring seamless communication and secure data exchange.

## Project Overview

The medium-sized business comprises three sites with varying numbers of rooms and hosts:

- **Site A:** 6 rooms with a total of 350 hosts. There are two networks: one with 300 hosts and another with 50 hosts accessible internally and externally.
- **Site B:** 1 room with 200 hosts.
- **Site C:** 4 rooms with 100 hosts.
In total, there are 650 workstations distributed over four separate networks.

## Network Components

### Routers
- **Site A Router 1:** Connects Site A to the internet and Site B. It has interfaces for connecting to other routers, internal networks, and the ISP.
- **Site A Router 3:** Connects Site A to Site C and the Firewall. It also links back to Site A Router 1 and contains interfaces for internal and external connections.
- **Site B Router 2:** Connects Site B to Site A. It has interfaces for internal connections.
- **Site C Router 4:** Connects Site C to Site A. It has interfaces for internal connections.

### Firewall
- **Firewall:** Provides security between the internal network and external connections. It has interfaces for connecting to routers and internal networks.

### Switches
- **48, 24, and 8-port switches:** Utilized for connecting workstations within each site.

## Network Topology

![image](https://github.com/Andresa1897/NetworkDesignProject/assets/98703359/13aa1cdf-d3cd-411c-846e-d7f33a1c5176)
![image](https://github.com/Andresa1897/NetworkDesignProject/assets/98703359/c0b69caa-cfd7-4560-bb3d-762215a49a1b)
![image](https://github.com/Andresa1897/NetworkDesignProject/assets/98703359/91a75d02-674d-4dd5-843d-47f003a7cb2c)
![image](https://github.com/Andresa1897/NetworkDesignProject/assets/98703359/740629e0-3788-40bb-9d5b-959f209a0fd5)

## Connectivity Details

- **Site A Router 1:**
  - Interfaces: Gi0/0 (Link to SITE A Router 3), Gi0/1 (Internal Network 128.64.236.0/23), Gi0/2 (Link to Site B Router 2), Gi0/3 (Unused)
  
- **Site A Router 3:**
  - Interfaces: Gi0/0 (Link to Site C Router 4), Gi0/1 (Link to Firewall ETH0), Gi0/2 (Link to Site A Router 1), Gi0/3 (Link to ISP)

- **Site B Router 2:**
  - Interfaces: Gi0/0 (Link to Site A Router 1), Gi0/1 (Internal Network 128.64.238.0/24), Gi0/2 (Unused), Gi0/3 (Unused)

- **Site C Router 4:**
  - Interfaces: Gi0/0 (Internal Network 128.64.239.0/25), Gi0/1 (Link to Site A Router 3), Gi0/2 (Unused), Gi0/3 (Unused)

- **Firewall:**
  - Interfaces: eth0 (Link to Site A Router 3), eth1 (Internal Network 128.64.239.128/26)

## Network Design

The network design ensures seamless connectivity between the sites while maintaining security and efficient data exchange. Each site's internal layout and external connectivity are optimized to meet the business's specific requirements.
