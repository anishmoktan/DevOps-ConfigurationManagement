# DevOps-ConfigurationManagement

## Ansible
- Allows us to write code to install and deploy multiple servers consistently.
  - Instructions to automate IT setup
  - Configuration Management: consistency of all systems in the infrastructure is maintained 
  - Automatic Deployment: applications are deployed automatically on a variety of environments
  
 - Push Configuration Tool:
  - Ansible is installed in the local machine server and it pushes configurations to the nodes (servers connected to the main local machine) through an SSH client
  - Local machines hold:
    - Modules: collections of configuration code files (also known as playbooks)
    - Inventory: document that groups the nodes under specific labels
    
 - Playbook:
  - The core where the architecture is defined, where instructions for configure nodes are written in YAML files
    - YAML files define the specific tasks for each node to configure the desired state
    
 - Inventory: 
   - Maintains the structure of the nodes' environment by classifying nodes into groups (manages physical hardware)
   - Hostnames of the nodes are specified under the group name

  
## Cloud Formation

## Terraform
