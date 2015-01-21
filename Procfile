# Use goreman to run `go get github.com/mattn/goreman`
#  To simplify bootstrap, I remove the 4th node ###One of the four etcd members falls back to a proxy
etcd2: etcd -name infra2 -listen-client-urls http://172.17.42.1:4002 -advertise-client-urls http://172.17.42.1:4002 -listen-peer-urls http://172.17.42.1:7002 -initial-advertise-peer-urls http://172.17.42.1:7002 -initial-cluster infra2=http://172.17.42.1:7002,infra3=http://172.17.42.1:7003,infra4=http://172.17.42.1:7004 \
       -initial-cluster-state new
etcd3: etcd -name infra3 -listen-client-urls http://172.17.42.1:4003 -advertise-client-urls http://172.17.42.1:4003 -listen-peer-urls http://172.17.42.1:7003 -initial-advertise-peer-urls http://172.17.42.1:7003 -initial-cluster infra2=http://172.17.42.1:7002,infra3=http://172.17.42.1:7003,infra4=http://172.17.42.1:7004 \
       -initial-cluster-state new
etcd4: etcd -name infra4 -listen-client-urls http://172.17.42.1:4004 -advertise-client-urls http://172.17.42.1:4004 -listen-peer-urls http://172.17.42.1:7004 -initial-advertise-peer-urls http://172.17.42.1:7004 -initial-cluster infra2=http://172.17.42.1:7002,infra3=http://172.17.42.1:7003,infra4=http://172.17.42.1:7004\
  -initial-cluster-state new

