# Ansible Playbook for Managing Zabbix Agent

These Ansible playbooks are designed to automate the management of the Zabbix agent on remote servers. The Zabbix agent enables monitoring and data collection from these servers by the Zabbix monitoring system.

## Prerequisites

Before using this playbook, make sure you have:

1. Ansible installed on your control machine.
2. SSH access to the target servers with sudo privileges.

## Usage

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Kartikdudeja/ansible-playbook-zabbix-agent.git
   ```
   
2. Navigate to the playbook directory:

   ```bash
   cd ansible-playbook-zabbix-agent
   ```
3. Update the `inventory.yml` file with the details of the servers you want to install Zabbix agent on.

4. Run the playbook:

   ```bash
   ansible-playbook -i inventory.yml install_zabbix_agent.yml
   ```

5. The playbook will connect to the remote servers, install the Zabbix agent, and configure it to communicate with the specified Zabbix server.

## Playbook Structure

- `install_zabbix_agent.yml`: Main playbook file, includes tasks for installing and configuring the Zabbix agent.
- `uninstall_zabbix_agent.yml`: Playbook for uninstalling zabbix agent and removing zabbix agent config file.
- `zabbix_agent2_config_allowkey.yml`: Updating zabbix agent config file to allow 'system.run' Item key.

## Customize

You can further customize the playbook according to your needs by modifying the variables, adding tasks, or adjusting templates.

## Disclaimer

This playbook is provided as-is and without warranty. Use it at your own risk. Review and test the playbook in a controlled environment before deploying it in a production setting.
