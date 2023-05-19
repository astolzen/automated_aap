# Automated AAP Controller Rollout & Configuration on Openshift

This Setup to be run on the CLI with "ansible-navigator" (or legacy "ansible-playbook") will:
 - Connect to an Openshift Cluster
 - Rollout an AAP Controller in the given Namespace using the AAP Operator
 - Add a subscription to the Controller
 - Create the Controller Configuration with Org, Secrets, Project and Templates based on the content of the vars.yml

### Prequisites:
  - An Openshift Cluster 
  - Installed AAP Operator

These Playbooks are to be used as skeleton. Modirfy and adjust the variable Structure and/or functionality as needed.

### Known Issues (WiP):
 - as of this version, the Playbook does not create an Inventory. This needs to be fixed so that the template loop can actually work

### Usage:
 - Modify vars.aml and secrets.yml as needed
 - Add manifest, add kubeconfig to the folder
 - run aap.yml to create the controller
 - run cleanup.yml to remove it

