### AWS VPC Module

This module creates following resources.
* VPC
* Internet Gateway with VPC association
* 2 Public subnets in 1a and 1b 
* 2 Private subnets in 1a and 1b
* 2 Database subnets in 1a and 1b
* Elastic IP
* NAT Gateway in 1a public subnet
* public Route table
* private Route table
* Database route table
* Subnets and rotue table associations
* VPC peering if user requests
* Adding the perring route in default VPC, if user don't provide acceptor VPC explicitly.
* Adding the peering routes in public private and database route tables.


### Inputs
* project_name (Required) - your Project name
* environment (Required) - which environment you are working in
* vpc_cidr (optional) - Default value is 10.0.0.0/16, user can override
* enable_dns_hostnames (optional) - Default value is true
* common_tags (optional) - better to provide
* vpc_tags (optional) - 
* igw_tags (optional) -
* public_subnets_cidr (Required) - user must provide 2 valid public subnets CIDR
* public_subnets_tags (optional) -
* private_subnets_cidr (Required) - user must provide 2 valid private subnets CIDR
* private_subnets_tags (optional) -
* database_subnets_cidr (Required) - user must provide 2 valid database subnets CIDR
* database_subnets_tags (optional) -
* nat_gateway_tags (optional) - 
* public_route_table_tags (optional) -
* private_route_table_tags (optional) -
* database_route_table_tags (optional) -
* is_peering_required (optional) - default value is false
* acceptor_vpc_id (optional) - default value is default VPC ID
* vpc_peering_tags (optional) - default value is empty, type is map.


### Outputs
* vpc_id - VPC ID created
* public_subnet_ids - 2 public subnet ID created
* private_subnet_ids - 2 private subnet ID created
* database_subnet_ids - 2 database subnet ID created

