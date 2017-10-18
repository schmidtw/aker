[![Build Status](https://travis-ci.org/Comcast/aker.svg?branch=master)](https://travis-ci.org/Comcast/aker)
[![codecov.io](http://codecov.io/github/Comcast/aker/coverage.svg?branch=master)](http://codecov.io/github/Comcast/aker?branch=master)
[![Apache V2 License](http://img.shields.io/badge/license-Apache%20V2-blue.svg)](https://github.com/Comcast/aker/blob/master/LICENSE)

# aker

Aker is a parental control experiment.

# Building and Testing Instructions

```
mkdir build
cd build
cmake ..
make
make test
```

# Running Example

Assumes that parodus is running at `tcp://127.0.0.1:6666`.  In this case the
`--firewall-cli` is going to echo the MAC addresses.

```
$ ./aker --parodus-url tcp://127.0.0.1:6666 \
         --client-url tcp://127.0.0.1:6600 \
         --firewall-cli echo \
         --data-file /tmp/aker-schedule.msgpack \
         --md5-file /tmp/aker-schedule.md5
```
