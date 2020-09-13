# Automate Instance and Apache Server on GCP using Ansible

## Description
The goal of this repository is to create a instance on GCP and deploy apache server on that instance using ansible playbook.  


## Prerequisites
1. Create [Project](https://console.cloud.google.com/projectselector/compute/instances) on Google Cloud Platform. 
2. Create a [Serviceaccount](https://console.cloud.google.com/iam-admin/serviceaccounts) with editor permission. (Refer [Creating-service-account](https://cloud.google.com/compute/docs/access/create-enable-service-accounts-for-instances))


## Getting Started !!
1. Install python version >= 2.6
```
$ sudo yum install python-pip
```
2. The GCP modules require both the requests and the google-auth libraries to be installed.
```
$ sudo pip install requests google-auth
```
3. Install Ansible
```
$ sudo pip install ansible 
```
4. Download [.JSON credentials file](https://support.google.com/cloud/answer/6158849?hl=en&ref_topic=6262490#serviceaccounts) of created service account.
5. Edit project ID, .JSON file path in vars/vars.yml file.
6. Run the Playbook 
```
$ ansible-playbook playbook/gce.yml
```
7. Your Google Compute Engine Instance is now created.
8. Browse to instance public ip.
