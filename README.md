# ansible-mongodb-cluster
MÔ HÌNH MONGODB CLUSTER 3 NODE: 1 Config Server, 1 Query Router, 1 Shard

# deploy
ansible-playbook -i mongodb.hosts mongodb.yml --tags setup

ansible-playbook -i mongodb.hosts mongodb.yml --tags config

ansible-playbook -i mongodb.hosts mongodb_bootstrap.yml

# thứ tự ưu tiên boot VM
Node Shard -> Node Config Server -> Node Query Router 
