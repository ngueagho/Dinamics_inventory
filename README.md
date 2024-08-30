# Dinamics_inventory

In Ansible, the inventory is a list of systems on which you want to run tasks. Traditionally, this inventory is static, defined in a hosts file with the IP addresses or names of your machines. However, when working in dynamic environments like the cloud, where machines can be created and destroyed frequently, a static inventory quickly becomes obsolete.

A dynamic inventory is a solution to this problem. Instead of manually listing hosts, a dynamic inventory queries an external source for an updated list of hosts at any given time. These external sources can be cloud service APIs (like AWS, GCP, Azure), databases, or any other service capable of providing information about machines.
