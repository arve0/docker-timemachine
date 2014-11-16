# arve0/timemachine
Netatalk running in docker for time machine backups.

```
docker pull arve0/timemachine
docker run -e "PASSWORD=asdf" -v /host/mnt/backup:/backup -p 548:548 --net=host -d arve0/timemachine
```

Connect with timemachine:asdf. If environment variable `PASSWORD` is not set, *timemachine* is the default password.

# notes on bonjour/avahi/zeroconf
[Network discovery](http://en.wikipedia.org/wiki/Bonjour_(software)) only works if afp daemon is on same network as client. Therefore `--net=host` is required if you would like the disk to show in Finder. If you don't need this, you can remove `--net=host` and connect with `cmd+k` -> `afp://hostname/`

Note that `--net=host` doesn't work with ubuntu trusty 14.04: https://github.com/docker/docker/issues/5899

# ideas from
- https://bitbucket.org/lonix/plex/src
- https://github.com/bySabi/dockerfiles/tree/master/nas
- https://github.com/aequitas/timemachine
