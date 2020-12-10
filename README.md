# One_Click_K8s_Cluster
With this we can easily setup 3 node Kubernetes cluster on a go

STEP 1 - make sure you have ansible installed on your device and all the nodes are password less [Key based Auth].

STEP 2 - insert ip and hostname details inside 'inventory' file
Example-
192.168.200.23
192.168.200.24
192.168.200.25


STEP 3 - insert host entries for /etc/hosts for all nodes in hosts.j2 file
Example-
192.168.200.23 master-node
