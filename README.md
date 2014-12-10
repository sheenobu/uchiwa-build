## Uchiwa Build

This project builds packages for Uchiwa, a Sensu dashboard.
Vagrant, Test-Kitchen and ServerSpec are used to create and test the packages.

The RPM and DEB packages are built on CentOS 6.5 x86_64, which cross-compile the Uchiwa binary to 32 & 64 bits.

The packages are tested on the following platforms:
- CentOS 5.11 x86_64
- CentOS 6.5 x86_64
- CentOS 6.5 i386
- Ubuntu 10.04 amd64 (currently disabled on this branch)
- Ubuntu 12.04 amd64 (currently disabled on this branch)
- Ubuntu 14.04 amd6  (currently disabled on this branch)
- Ubuntu 14.04 i386  (currently disabled on this branch)

### Run

```
export UCHIWA_VERSION=0.3.0
export BUILD_NUMBER=1
kitchen converge build
kitchen destroy build
kitchen test test
```

### Run from master uchiwa

```
export UCHIWA_VERSION=0.5.0-dev
export BUILD_NUMBER=1
export UCHIWA_REVISION=master
kitchen converge build
kitchen destroy build
kitchen test test
```
