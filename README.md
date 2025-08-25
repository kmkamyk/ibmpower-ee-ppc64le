# IBM Power Execution Environment

This repository contains the definition of a custom **Ansible Execution Environment (EE)** focused on managing **IBM Power Systems** (HMC, AIX, VIOS, IBM i, PowerHA, PowerVC) and traditional UNIX/Linux environments.  
It is designed without cloud-related collections to stay lightweight and specialized.

## Features
- Based on CentOS Stream 9 with **Python 3.13**  
- Includes IBM Power Ansible collections:  
  - `ibm.power_hmc`
  - `ibm.power_aix`
  - `ibm.power_vios`
  - `ibm.power_ibmi`
  - `enfence.powerha_aix`
  - `ibm.powervc`
- Useful community collections for UNIX/Linux:  
  - `community.general`  
  - `community.crypto`  
  - `community.network`  
  - `ansible.posix`  
  - `ansible.utils`  

## Build locally
To build the EE image on your workstation:
```bash
pip install ansible-builder docker
ansible-builder build -t ee-ibmpower:latest -f execution-environment.yml
