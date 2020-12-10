STEP 1 - make all the nodes password less accessable with ssh-copy id command

STEP 2 - insert ip and hostname details inside 'inventory' file
Example-
Master server ip -192.168.200.23 - master-node
Worker server ip - 192.168.200.24-worker-node-1 ,192.168.200.25-worker-node-2


STEP 3 - insert host entries for /etc/hosts for all nodes in hosts.j2 file
Example-
192.168.200.23 master-node
192.168.200.24 node-1 worker-node-1
192.168.200.25 node-2 worker-node-2

ifconfig | grep eth0 -A 1 | grep inet | awk {'print $2'}

#Find the node
kubectl get nodes
#Drain it
kubectl drain nodetoberemoved
#Delete it
kubectl delete node nodetoberemoved
On Worker Node (nodetoberemoved). Remove join/init setting from node



Get join token = kubeadm token create --print-join-command   