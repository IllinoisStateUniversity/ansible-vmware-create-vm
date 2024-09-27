# VMware - Create VM

This playbook automates the process of creating virtual machines (VMs) in VMware environments using Ansible Automation Platform. It supports various configurations and environments by utilizing variables from both user inputs and predefined files.

## Prerequisites

Before you can run this playbook, you need the following:
- Ansible Automation Platform - Ansible Controller.
- Access to a VMware vSphere environment.
- The `community.vmware` collection installed and its prerequistes installed in your execution environment.

## Configuration

The playbook uses several variables defined in `vars/prod.yml` for production environments and `vars/test.yml` for test environments. These files include details about the vSphere environment like hostname, datacenter, and cluster configurations.

### Variable Files

- `vars/prod.yml`: Contains variables for the production environment.
- `vars/test.yml`: Contains variables for the test environment.

## Usage


## Playbook Tasks
- **Create VM**: Creates a new virtual machine based on the specifications provided through survey variables and additional configurations defined in the variable files.
- **Save VM Info for Workflow Use**: Saves newly created VM information for later use in a workflow.
- **Add Tags**: Assigns metadata tags to the newly created VM within the vSphere environment to be used in Ansible inventories.

## Survey Variables
These are additional variables that need to be provided by the user during the execution of the playbook, typically through an AAP survey.

- **survey_hostname**: The hostname of the VM.
- **survey_resourceowner**: The owner of the resource.
- **survey_environment**: The environment of the VM (prod, test, etc.).
- Additional hardware specifications like CPU, memory, and disk size.
