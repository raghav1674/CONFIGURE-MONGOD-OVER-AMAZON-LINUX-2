# CONFIGURE MONGOD OVER AMAZON LINUX 2
# MAP REDUCE CLUSTER CONFIGURED USING ANSIBLE:

## Create vars folder, inside that create two files secret.yaml and instance_vars.yaml: 

- vars/secret.yaml:
  ----------------
  
     AWS_ACCESS_KEY_VAL: AWS ACCESS KEY

     AWS_SECRET_KEY_VAL: AWS SECRET KEY


- vars/instance_vars.yaml:
  -----------------------

 	key: KEY NAME

	type_instance: t2.micro

	subnet_id: SUBNET ID

	region_id: ap-south-1

	security_group_id: SECURITY GROUP ID

	inventory_path: inventory

	ami_id: ami-068d43a544160b7ef

	has_public_ip: true


## HOW TO RUN THIS ANSIBLE PLAYBOOKS:

 - Run the ec2_config.yaml file first. 
   > ansible-playbook ec2_config.yaml
 
 - Run the tasks/main.yaml file only. 
   > ansible-playbook tasks/configure_mongod_on_AMAZON_LINUX_2.yaml
