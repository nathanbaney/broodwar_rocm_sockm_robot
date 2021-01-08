# broodwar_rocm_sockm_robot

/* HINDSIGHT OVERVIEW / RESUME INFORMATION

Another case of school ending a nice summer project... even got pretty far with the guts of 
this one too. Although, in retrospect, I only really got the the part where I interfaced the two 
BroodWar agents against one another, and didn't even get to the "fun" machine learning part.
Would have been 1000% times easier if I had an Nvidia GPU, or access to a cloud cluster.
In hindsight, I don't think the central concept I had at the time would have worked anyways
(having increasingly large neural networks being trained sequentially with hand-curated
scenarios). Combining NNs just isn't as simple as stapling them together.

*/

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
