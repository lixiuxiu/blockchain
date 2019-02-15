## fabric 1.1.0镜像

sudo docker pull hyperledger/fabric-tools:x86_64-1.1.0
sudo docker pull hyperledger/fabric-couchdb:latest
sudo docker pull hyperledger/fabric-kafka:latest
sudo docker pull hyperledger/fabric-orderer:x86_64-1.1.0
sudo docker pull hyperledger/fabric-peer:x86_64-1.1.0
sudo docker pull hyperledger/fabric-ca:x86_64-1.1.0
sudo docker pull hyperledger/fabric-ccenv:x86_64-1.1.0
sudo docker pull hyperledger/fabric-baseimage:x86_64-0.4.6
sudo docker pull hyperledger/fabric-baseos:x86_64-0.4.6
sudo docker pull hyperledger/fabric-zookeeper:latest
sudo docker pull hyperledger/fabric-javaenv:x86_64-1.1.0
sudo docker pull hyperledger/fabric-membersrvc:latest

sudo docker tag hyperledger/fabric-baseimage:x86_64-0.4.6 hyperledger/fabric-baseimage:latest
sudo docker tag hyperledger/fabric-baseos:x86_64-0.4.6 hyperledger/fabric-baseos:latest
sudo docker tag hyperledger/fabric-ccenv:x86_64-1.1.0 hyperledger/fabric-ccenv:latest
sudo docker tag hyperledger/fabric-javaenv:x86_64-1.1.0 hyperledger/fabric-javaenv:latest
sudo docker tag hyperledger/fabric-peer:x86_64-1.1.0 hyperledger/fabric-peer:latest
sudo docker tag hyperledger/fabric-tools:x86_64-1.1.0 hyperledger/fabric-tools:latest
sudo docker tag hyperledger/fabric-ca:x86_64-1.1.0 hyperledger/fabric-ca:latest
sudo docker tag hyperledger/fabric-orderer:x86_64-1.1.0 hyperledger/fabric-orderer:latest