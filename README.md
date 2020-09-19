# Automate Instance and Apache Server on GCP using Ansible

## Description
The goal of this repository is to create a instance on GCP and deploy apache server on that instance using ansible playbook.  


## Prerequisites
1. Create [Project](https://console.cloud.google.com/projectselector/compute/instances) on Google Cloud Platform. 
2. Create a [Serviceaccount](https://console.cloud.google.com/iam-admin/serviceaccounts) with editor access. (Refer [Creating-service-account](https://cloud.google.com/compute/docs/access/create-enable-service-accounts-for-instances))


## Getting Started !!
1. Install python version > 3.0
```
$ sudo yum install python3-pip
```
2. The GCP modules require both the requests and the google-auth libraries to be installed.
```
$ sudo pip3 install requests google-auth
```
3. Install Ansible
```
$ sudo pip3 install ansible 
```
4. Download [.JSON credentials file](https://support.google.com/cloud/answer/6158849?hl=en&ref_topic=6262490#serviceaccounts) of created service account.
5. Edit instance_name in [vars/main.yml](vars/main.yml), by default it is centos-7.
6. Edit machine_type in [vars/main.yml](vars/main.yml), by default it is e2-micro.
7. Edit zone in [vars/main.yml](vars/main.yml), by default it is us-central1-a.
8. Edit source_image in [vars/main.yml](vars/main.yml), by default it is CENTOS-7.
5. Give project id, .JSON file_path in [vars/main.yml](vars/main.yml) file. 
7. Run the Playbook 
```
$ ansible-playbook gce.yml
```
8. Your Google Compute Engine Instance is now created, with Apache Server installed in it.
9. Browse to instance public ip address.
