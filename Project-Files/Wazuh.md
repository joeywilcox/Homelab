# File Integrity Monitoring with Wazuh
## Overview
This page documents my experience with Wazuh when exploring in my homelab. This project stemmed from a need in my day job to implement FIM and free ninty-nine fit the budget requirements.
## Project Completion Date 🏁
**August 2023**
## Process
1. Before I begin, I explored the Wazuh documentation extensively to discover the purpose of FIM, how Wazuh achieves FIM, system requirements, and deployment steps.
2. I spun up three separate virtual Linux servers in Proxmox to serve as the distributed cluster for Wazuh and ensured they were all configured and communicating correctly.
3. At this point, I needed to see if the cluster would pick up on changes from a deployed client.
4. To do this, I spun up another virtual machine to act as a Windows client and installed the Wazuh agent.
5. I then scripted out a short loop to create, modify, then delete a file to give Wazuh some activity to pick up on. It worked!
6. After reviewing some additional documentation I discovered an all-in-one distribution model that took the three machines I used earlier and contained them into a single VM.
7. I kept my Windows client and tore down the distributed 3 machine cluster and spun up a clean VM to use as the all-in-one machine. This went well and as expected.
8. Finally, I used the same script as before to test both the all-in-one distribution and alerting rules!
