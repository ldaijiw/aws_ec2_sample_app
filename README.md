# AWS

## The Cloud

Cloud computing is the on-demand availability of computer system resources, especially data storage (cloud storage) and computing power, without direct active management by the user.

**DevOps and the Cloud**

- Will make sure we use cloud to our advantage
	- Can expand if it is successful
	- Reduce if we don't get traction needed
	- All without committing large quantities of cash, possibly endangering other sections of the business
	- Shared responsiblity model: 
		- Amazon responsible for security of the cloud (mostly physical)
		- User is responsible for security inside your cloud and how it interacts with the outside

**Capital Expenditure vs. Operational Expenditure**

## AWS

Amazon Web Servers is a public cloud provider, offering 175 fully featured services from data centers placed around the globe

AWS offer infrastructure technologies like compute, storage, and databases as well as emerging technologies, such as machine learning and artificial intelligence, data lakes and analytics, and Internet of Things.

## Setting Up an Instance on EC2

**Amazon Elastic Compute Cloud (EC2) provides scalable computing capacity in the AWS cloud**

- EC2 eliminates need to invest in hardware up front, so businesses can develop and deploy applications faster
- EC2 can launch any number of virtual servers as needed, as well as security, networking, and storage configuration
- EC2 enables businesses to scale up or down to handle changes in requirements or spikes in popularity, reducing the need to forecast traffic

### Security Groups

A security group acts as a virtual firewall for an EC2 instance to control inbound and outbound traffic
- Security groups act at the instance level, not subnet level, therefore each instance within a subnet can be assigned to a different set of security groups
- For each security group, add rules that control the inbound traffic to instances, and a separate set of rules that contorl the outbound traffic
	- Can specify allow rules, but not deny rules
	- Can specify separate rules for inbound and outbound traffic
	- SGs enable to filter traffic based on protocols and port numbers
	- By default, there are no inbound rules, i.e. no inbound traffic originating from another host to instance is allowed
	- By default, all outbound traffic is allowed

For this project, there are a few inbound rules that were to be configured:
| Type | Source | Port | Description |
| :--: | :----: | :--: | :---------: |
| SSH | My IP | 22 | Port 22 Home |
| TCP | My IP | 3000 | Port 3000 Home |
| HTTP | 0.0.0.0/0 | 80 | Port 80 for everyone |


