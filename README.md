# IBM Power Execution Environment (EE) for PPC64LE

This repository contains the definition of a custom **Ansible Execution Environment (EE)** focused on managing **IBM Power Systems** (HMC, AIX, VIOS, IBM i) and traditional UNIX/Linux environments.

It has been specifically tailored for the **`ppc64le`** architecture and includes a **minimized set of packages** to facilitate the compilation of Python libraries on this platform. The project is intentionally designed without cloud-related collections to stay lightweight and specialized.

## Features
- Based on **CentOS Stream 9** with **Python 3.11**.
- Includes key Ansible collections for IBM Power:
  - `ibm.power_hmc`
  - `ibm.power_aix`
  - `ibm.power_vios`
  - `ibm.power_ibmi`
- Includes essential community collections for UNIX/Linux:
  - `community.general`
  - `ansible.posix`

## Build locally
To build the EE image on your workstation:```bash
pip install ansible-builder docker
ansible-builder build -t ee-ibmpower-ppc64le:latest -f execution-environment.yml
```
