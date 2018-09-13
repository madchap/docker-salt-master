docker-salt-master
=============

* map ssh config for git repo RO access
* copy fileserver.conf (or map) to /etc/salt/master.d

```
docker run --name salt-master --restart=unless-stopped -v $PWD/root-ssh-config:/root/.ssh/config:ro -v salt_master_config:/etc/salt -v salt_master_data:/data -p 4505:4505 -p 4506:4506 -p 4443:443 madchap/docker-salt-master:0.1
```
