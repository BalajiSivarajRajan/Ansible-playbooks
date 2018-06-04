# Ansible-playbooks
What is Ansible?
  Ansible is a radically simple IT automation engine that automates cloud provisioning, configuration management, application deployment, intra-service orchestration, and many other IT needs
  
Why Ansible? 
  Its an agentless and requires no additional custom security infrastructure, so it's easy to deploy - and most importantly, it uses a very simple language (YAML, in the form of Ansible Playbooks) that allow you to describe your automation jobs in a way that approaches plain English.

How it works?
  Ansible works by connecting to the nodes and pushing out small programs, called "Ansible modules". These programs are written to be resource models of the desired state of the system. Ansible then executes these modules (over SSH by default), and removes them when finished.
  
