## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

<img width="791" alt="Diagram Project 1" src="https://user-images.githubusercontent.com/90808588/156683000-56e4d426-ec5f-4c7c-844a-7ae9ad32a792.png">
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _YML____ file may be used to install only certain pieces of it, such as Filebeat.

  ELK install
  Metricbeat Playbook
  Filebeat Playbook
This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _avaliable____, in addition to restricting ___Access__ to the network.
-Load balancers help ensure environment availability through distribution of incoming data to web servers. Jump boxes allow for more easy administration of multiple systems and provide an additional layer between the outside and internal assets.
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _configuration files____ and system _files____.
 Filebeat watch for Log files or log events
 Metricbeat record Metrics from on going services on the server

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.
| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web-1    | Webserver| 10.0.0.11  | Linux            |
| Web-2    | Webserver| 10.0.0.12  | Linux            |                  
| Web-3    | Webserver| 10.0.0.13  | Linux            |
| VM-ELK   | Webserver| 10.1.0.4   | Linux            |  
| Name     | Function | IP Address | Operating System |


### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the jump-box-Provisioner machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

Machines within the network can only be accessed by _Jumpbox____.
 The Elk Machine can have access from personal IP address A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.1 10.0.0.2    |
|  Web-1   | No                  |  172.56.11.249       |
|  Web-2   | No                  |  172.56.11.249       |
|  Web-3   | No                  |  ,, ,, ,, ,,         |
|  VM_ELK  | Yes(http)           |  ,, ,, ,, ,,         |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- The main advantage is  It is flexible because it allows changes to be made within any of the VMs associated with it.
The playbook implements the following tasks:
- elk stack together
- Monitors the server
*Command to Execute playbook
-sudo ansible-playbook site.yml

 1. Install Docker.io
  2. Install python3-pip
  3. Install Docker Python Module
  4. Download and launch a Docker web container


### Target Machines & Beats
This ELK server is configured to monitor the following machines:
-Web 1
-Web 2
- _TODO: 10.0.0.1 10.0.0.11 10.0.0.12 10.0.0.13 10.0.0.4We have installed the following Beats on these machines:
- _TODO: we have successful installed Filebeat and MetricbeatThese Beats allow us to collect the following information from each machine:
- _TODO: Filebeat monitors log files and log events. While Metricbeat looks out for any information in the file
system which has been manipulated. ### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the ansible configuration file to Run playbook.
- Update the __ansible host___ file to include the IP address of the Elk Server VM and webservers.
- - Run the playbook, and navigate to __jumpbox__ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _the playbook file is The Filebeat-configuration & you copy it /etc/ansible/files/filebeat-config.yml to /etc/filebeat/filebeat.yml 
- The elk-playbook.yml is the file 
- - _Which file do you update to make Ansible run the playbook on a specific machine? elk-playbook.yml file-
-   How do I specify which machine to install the ELK server on versus which to install Filebeat on?_we could use the IPs server.
-   - _Which URL do you navigate to in order to check that the ELK server is running?
- http://[your.ELK-VM.External.IP]:5601/app/kibana.
_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
