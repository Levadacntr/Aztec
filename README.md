sudo apt install screen -y && screen -Rd aztec
sudo systemctl restart aztecd
curl -s -X POST -H 'Content-Type: application/json' -d '{"jsonrpc":"2.0","method":"node_getL2Tips","params":[],"id":67}' http://localhost:8080 | jq -r ".result.proven.number"
curl -s -X GET -H 'accept: application/json' 'https://api.testnet.aztecscan.xyz/v1/temporary-api-key/l2/latest-height' | jq    
sudo systemctl stop aztecd
~/.aztec/bin/aztec -V
