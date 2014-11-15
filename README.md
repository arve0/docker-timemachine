# arve0/timemachine
Netatalk running in docker for time machine backups.

```
docker pull arve0/timemachine
docker run -e "PASSWORD=asdf" -p 548:548 --net=host arve0/timemachine
```

Connect with timemachine:asdf. If environment variable PASSWORD is not set, 'timemachine' is the default password.


# ideas from
https://bitbucket.org/lonix/plex/src
https://github.com/bySabi/dockerfiles/tree/master/nas
https://github.com/aequitas/timemachine
