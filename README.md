Interview for Bridgewell Sys&Data Team
=====================================

# 1
Please explain this command.
```
docker rmi $(docker images | grep "^<none>" | awk "{print $3}")
```

# 2
Please explain this command.
```
docker run \
	-d \
	-e TEST_ENV=HELLO_WORLD \
	-v /etc/localtime:/etc/localtime:ro \
	-p 8080:80 \
	-p 5566:443 \
	--link mysql:db \
	--dns=10.0.0.1 \
	--dns=192.168.0.1 \
	--dns-search=local.test.com \
	--dns-search=test.com \
	--name test_docker \
	registry.local.test.com/infra/test_docker:0-17.08.03-caf85b05-rc
```

# 3
Please explain the functionality of following two files in `Linux-like` operation system.
```
/etc/hosts
/etc/resolv.conf
```

# 4
Please write a `bash script` to read `access.log` in this repo; find out the log with 404 `return code`; count them group by IP.

expected output:
```
1 118.163.135.13
1 123.51.165.114
1 210.242.60.1
1 210.243.21.253
1 220.134.215.89
1 59.125.23.30
1 60.250.66.98
1 74.222.14.82
3 64.71.171.80
4 64.71.171.86
```

# 5
Please explain following commands
```
git add
git commit
git push
git fetch
git pull
git checkout
git branch
git revert
git rebase
git reset
```

# 6

Please describe your findings according to the following datasets respectively.

## Dataset 1

* [dataset1.tar.gz](dataset1.tar.gz)
* list of user agent

```
Mozilla/5.0 (Windows NT 10.0; WOW64;  ....
Mozilla/5.0 (Linux; Android 7.0; SAMS ....
Mozilla/5.0 (Windows NT 6.3; Win64; x ....
Mozilla/5.0 (Windows NT 6.1) AppleWeb ....
Mozilla/5.0 (iPhone; CPU iPhone OS 10 ....
```

## Dataset 2

* [dataset2.gz.parquet](dataset2.gz.parquet)
* timestamp (in micro second) and hashed user id extracted from user visit event logs

```
+-------------------+----------------+
|timestamp_micro_sec|         user_id|
+-------------------+----------------+
|   1501545994088866|c77d0bcc55b624b7|
|   1501545992833956|c7dd2406697ceb0b|
|   1501545996724693|cd6ba573a1ea9ea4|
|   1501545996246811|c2abe46567acd437|
|   1501545994870040|c3c79186379f219f|
+-------------------+----------------+
only showing top 5 rows

```

----------

*Hints:*

* there are some useful utility packages you may need, ex. [user-agents](https://pypi.python.org/pypi/user-agents)
* try to do some discovering, cleaning or analysis
