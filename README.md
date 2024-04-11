# podscripts_elk

## Sample configs
* https://github.com/elastic/elasticsearch/blob/v7.17.20/docs/reference/setup/install/docker-compose.yml
* https://github.com/elastic/elasticsearch/blob/v8.13.2/docs/reference/setup/install/docker/docker-compose.yml

## Synology tweaks
* ELK 8 requires SECCOMP. Synology DSM7 doesn't have this compiled into the kernel. Workaround is to use ELK7 and have `bootstrap.system_call_filter=false` set.
* Needs `vm.max_map_count=262144` set on the synology host `(ssh > sudo su)` in `/etc/sysctl.conf`
