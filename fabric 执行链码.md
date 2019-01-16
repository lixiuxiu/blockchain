```
//初始化 

peer chaincode instantiate -o orderer.wisedu.com:7050 -C mychannel -n mycc8 -v 1.0 -c '{"Args":["init"]}' -P "OR('Org1MSP.peer','Org2MSP.peer','Org3MSP.peer')" //证书上链 peer chaincode invoke -o orderer.wisedu.com:7050 -C mychannel -n mycc8 -c '{"Args":["InitCert","uuid1","123456789@qq.com","hash","orignal"]}' 

//证书hash是否被篡改

 peer chaincode query -o orderer.wisedu.com:7050 -C mychannel -n mycc8 -c '{"Args":["ValidationOfHash","uuid1","hash"]}' 

//查询证书所有元素 

peer chaincode query -o orderer.wisedu.com:7050 -C mychannel -n mycc8 -c '{"Args":["QueryCert","uuid2"]}' 

//查询证书原件

 peer chaincode query -o orderer.wisedu.com:7050 -C mychannel -n mycc7 -c '{"Args":["QueryOriginalCert","uuid1"]}' 

//证书绑定

 peer chaincode invoke -o orderer.wisedu.com:7050 -C mychannel -n mycc8 -c '{"Args":["Certbinding","uuid1","did1"]}' 

//证书撤销 

peer chaincode invoke -o orderer.wisedu.com:7050 -C mychannel -n mycc7 -c '{"Args":["RollBack","uuid1","reason"]}'
```

