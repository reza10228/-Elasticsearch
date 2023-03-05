in Production mode:\
Set `vm.max_map_count` to at least **262144**\
The `vm.max_map_count` kernel setting must be set to at least 262144 for **production** use

`sysctl -w vm.max_map_count=262144`

The `vm.max_map_count` setting should be set permanently in **/etc/sysctl.conf**:\
 `grep vm.max_map_count /etc/sysctl.conf`\
vm.max_map_count=262144

To apply the setting on a live system, run:\
`sysctl -w vm.max_map_count=262144`

If change Directory mount point on docker-compose file must command under for specific directory 

For example /home/node1:/usr/share/elasticsearch/data

`sudo chown -R 1000:root /home/node1`