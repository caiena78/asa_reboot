
# Cisco ASA HA Failover Automation with Ansible

## 📌 Project Description
This project provides an **Ansible playbook** to automate high-availability (HA) operations on Cisco ASA firewalls.  
The workflow includes:
1. Logging into the **standby ASA**.
2. Triggering **failover active** to make the standby unit active.
3. Logging into the **active ASA**.
4. Executing **failover reload-standby** to reboot the new standby unit.

This automation helps streamline HA maintenance tasks, reduce manual errors, and improve operational efficiency.



## Running Instructions
    1. set enviroment variables
        export ASA_USER="admin"
        export ASA_PASSWORD="yourpassword"
    2. ansible-playbook asa_reboot.yml



