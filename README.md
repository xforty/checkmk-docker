# CheckMK in docker

We put together this simple checkmk image so we could easily use check_mk
in coreos and with docker. 

# Running It

docker run \
  --restart=always \
  --detach \
  --name=checkmk \
  --hostname=checkmk \
  -volume /var/run/docker.sock:/var/run/docker.sock \
  --publish 6556:6556 \
  xforty/checkmk
  
