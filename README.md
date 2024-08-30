# Dinamics_inventory

In Ansible, the inventory is a list of systems on which you want to run tasks. Traditionally, this inventory is static, defined in a hosts file with the IP addresses or names of your machines. However, when working in dynamic environments like the cloud, where machines can be created and destroyed frequently, a static inventory quickly becomes obsolete.

A dynamic inventory is a solution to this problem. Instead of manually listing hosts, a dynamic inventory queries an external source for an updated list of hosts at any given time. These external sources can be cloud service APIs (like AWS, GCP, Azure), databases, or any other service capable of providing information about machines.

How does it work?

    Inventory Script or Plugin: Ansible uses vendor-specific scripts or plugins to query an external source and obtain a list of hosts. For example, for AWS there is a Python script that queries the AWS API to get the list of EC2 instances.

    Dynamic Groups: Dynamic inventory can also group hosts based on certain criteria, for example, grouping all EC2 instances with a specific tag in AWS.

    Dynamic Host Variables: In addition to hosts, dynamic inventory can also retrieve specific host variables from the external source, such as an instance's public or private IP address, its tags, etc.
