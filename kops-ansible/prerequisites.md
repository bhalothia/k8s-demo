KOPS cluster setup on aws with Ansible

Server compatibility:  >= ubuntu 14.04

Prerequisites 

1. Install awcli and setup aws profile


pip install awscli --upgrade --user


Doc: https://docs.aws.amazon.com/cli/latest/userguide/installing.html


2. Insltall Ansible


Doc: http://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html



For Kops cluster deployment, We have to create an IAM user that has the below IAM attached policies/Permissions.


1. AmazonEC2FullAccess
2. AmazonRoute53FullAccess
3. AmazonS3FullAccess
4. IAMFullAccess
5. AmazonVPCFullAccess



The sequence of Playbook execution after installation of kubectl and kops packages.



1. Create a s3 bucket.



Note: Before executing the playbook, make sure to fill all the vars under roles/s3-bucket-creation/vars/main.yml


ansible-playbook  -i inventory/kops.yml s3-bucket-creation.yml



2. Kops cluster deployment.


Note: Before executing the playbook, make sure to fill all the vars under roles/kops-cluster/vars/main.yml


ansible-playbook -i inventory/kops.yml kops-cluster.yml
