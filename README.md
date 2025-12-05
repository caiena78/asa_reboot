
# Cisco ASA HA Failover Automation with Ansible

## 📌 Project Description
This project provides an **Ansible playbook** to automate high-availability (HA) operations on Cisco ASA firewalls.  
The workflow includes:
1. Logging into the **standby ASA**.
2. Triggering **failover active** to make the standby unit active.
3. Logging into the **active ASA**.
4. Executing **failover reload-standby** to reboot the new standby unit.

This automation helps streamline HA maintenance tasks, reduce manual errors, and improve operational efficiency.

## building a virtual enviroment and installing dependancies
    sudo apt update
    sudo apt install -y python3 python3-venv python3-pip git build-essential
    git clone  https://github.com/caiena78/asa_reboot.git
    cd asa_reboot
    python3 -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip setuptools wheel
    pip install "ansible>=9.0.0"
    pip install paramiko cryptography
    ansible-galaxy collection install cisco.asa
    ansible-galaxy collection install ansible.netcommon


## Running Instructions
    1. set enviroment variables
        export ASA_USER="admin"
        export ASA_PASSWORD="yourpassword"
    
    2. update the ip's of the Active and Standby ASA's in hosts.yml

    3. ansible-playbook asa_reboot.yml



