# Ansible-ACI-Multicloud
This repo consists of working examples of Ansible playbooks with use cases around Cisco ACI and Cisco Multi-Site Orchestrator (MSO)

This example use 3 roles:
  - 1. Multi-Site Orchestrator(MSO)
  - 2. vCenter 
  - 3. cAPIC
  
## MSO:
    This roles contains variables and tasks to create the policy for including epgs, contracts, filters for a 2 tier App to be pushed down to on-premis APIC and cloud APIC running on AWS.  It also spins up and EC2 instance running the web server and assigning it to the right EPG
    
## vCenter:
    This role contains variables and tasks to change the port group on an existing VM. 
    
## cAPIC:
    This role contains tasks to create an external EPG.
    
## Usage:
    Create a host file with appropriate multi-cloud env.
        
        [mso]
        mso1 host="" user="" pass=""

        [apic]
        onprem host="" user="" pass=""
        capicaws host="" user="" pass=""
        capicazure host="" user="" pass=""

        [vcenter]
        vc host="" user="" pass=""

   
 ## Run:
    ansible-playbook -i hosts site.yml
    
    
