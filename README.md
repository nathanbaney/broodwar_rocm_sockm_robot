# broodwar_rocm_sockm_robot
broodwar ml via rocm tensorflow, docker images, and spaghetti

The story thus far...
1. Installed clean Ubuntu 18.04 kernel
2. Install ROCm kernel
3. Install Docker
4. Find Starcraft Brood War MPQs
5. Make Dockerfile that extends the rocm/tensorflow image,
    clones and installs https://github.com/openbw/openbw
    and https://github.com/openbw/bwapi,
    copies MPQs, bwapi-data/bwapi.ini, and maps into bin,
    opens port 6112, 
    sets OPENBW_LAN_MODE to TCP,
    sets OPENBW_TCP_CONNECT_HOSTNAME to whatever your container name is
