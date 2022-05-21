# aws_vpc_module

VPC Module
Whats is the vpc module? This module creates a basic vpc.

How to use the vpc module? 
This module was created with one map variable with two indices:
Name = name of vpc
cidr_block = de cidr_block of the vpc

output available (vpc id)
The name of the variable is vpc_id it will be used for get the vpc id when they needed (for example to create the subnet)

To use this kind of variable in the module it's necessary create a instance of the variable on de main.tf, for example:

module "vpc" {<br>
  source = "git::https://github.com/BrunoHigino06/aws_vpc_module.git"<br>
<br>
  vpc = {<br>
    Name = "Main"<br>
    cidr_block = "10.0.0.0/16"<br>
  }<br>
}
