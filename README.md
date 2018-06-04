# Ansible-playbooks
## What is Ansible?
  Ansible is a radically simple IT automation engine that automates cloud provisioning, configuration management, application deployment, intra-service orchestration, and many other IT needs
  
## Why Ansible? 
  Its an agentless and requires no additional custom security infrastructure, so it's easy to deploy - and most importantly, it uses a very simple language (YAML, in the form of Ansible Playbooks) that allow you to describe your automation jobs in a way that approaches plain English.

## How it works?
  Ansible works by connecting to the nodes and pushing out small programs, called "Ansible modules". These programs are written to be resource models of the desired state of the system. Ansible then executes these modules (over SSH by default), and removes them when finished.
  
## Keys
  Though passwords are supported, preferred approach is to use SSH keys with ssh-agent as its one of the best ways to use Ansible.

## Inventory 
  By default, Ansible represents the machines it manages using a very simple INI file that puts all of the managed machines in groups of users. To add new machines, there is no additional SSL signing server involved and all its required is to update the inventory file. If there's another source of truth in the infrastructure, Ansible can also plugin to that, such as sources like EC2, Rackspace, OpenStack, etc.

  inventory file looks like:
```
         [webservers]
        www1.example.com
        www2.example.com

        [dbservers]
        db0.example.com
        db1.example.com
```

## Playbooks
  Its a simple and powerful automation language. Playbooks can finely orchestrate smaller part of the infrastructure topology, with very detailed control over how many machines to tackle at a time. 
  
  Playbook looks like:
 ``` 
      ---
    - hosts: webservers
        roles:
    - common
    - webapp


    - name: 
      package: 
```
## What Ansible can automate?
  Ansible can be used to automate three main task 
    - Server Provisioning 
    - Configuration management
    - Application Deployment 

## Conclusion
  Ansible can be used to automate the IT environments whether they are hosted on tradational bare metal, VM, cloud and it can automate the configuration of wide range of systems and devices such as databases, app servers, tools, etcs.
