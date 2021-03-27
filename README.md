# altgateway



plugins:
1. openvpn
2. softether
4. l2tp
5. tor
6. i2p
7. ipfs

interface:
1. gateway
2. http proxy
3. socks proxy
4. dns server

functions:
1. periodically detect connectivity and speed, switch traffic path
2. create a tun interface as local interface which connects to altgateway, so that local servies won't bind on gateway.
3. every l3vpn in dedicated network namespace so that ip address won't conflict
4. 

对于nm场景，在本地会包含3个接口（3个IP）：1. 上联物理口；2. altgateway上联口；3. fullmesh-vpn上联口
           如果有network-share，还会包含：下联物理口
对于rt场景，在本地只会包含：rt上联口；在rt-network-namespace中，会包含：上联物理口，下联物理口，altgateway上联口；fullmesh-vpn上联口



