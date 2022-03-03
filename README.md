## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Ansible file

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _effective____, in addition to restricting ___Access__ to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _configuration files____ and system _files____.
- _TODO: What does Filebeat watch for?_ They watch for Log files or log events
- - _TODO: What does Metricbeat record?_They record Metrics from on going services on the server

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
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _Jumpbox____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.1 10.0.0.2    |
|  Web-1   | No                  |  172.56.11.249       |
|  Web-2   | No                  |  172.56.11.249       |
|  Web-3   | No                  |  ,, ,, ,, ,,         |
|  VM_ELK  | Yes(http)           |  ,, ,, ,, ,,         |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_
- The main advantage is  It is flexible because it allows changes to be made within any of the VMs associated with it.
The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
-  1. Install Docker.io
  2. Install python3-pip
  3. Install Docker Python Module
  4. Download and launch a Docker web container
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: 10.0.0.1 10.0.0.11 10.0.0.12 10.0.0.13 10.0.0.4We have installed the following Beats on these machines:
- _TODO: we have successful installed Filebeat and MetricbeatThese Beats allow us to collect the following information from each machine:
- _TODO: Filebeat monitors log files and log events. While Metricbeat looks out for any information in the file
system which has been manipulated. ### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the ansible configuration file to Run playbook.
- Update the __ansible host___ file to include...
- Run the playbook, and navigate to __jumpbox__ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- The elk-playbook.yml is the file 
- - _Which file do you update to make Ansible run the playbook on a specific machine? elk-playbook.yml file-
-   How do I specify which machine to install the ELK server on versus which to install Filebeat on?_we could use the IPs server.
-   - _Which URL do you navigate to in order to check that the ELK server is running?
 http://[ElkProject1VM-ip]:5601/app/kibana
_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
