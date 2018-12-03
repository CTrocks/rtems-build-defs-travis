
# RTEMS Toolchain Build - Continious Integration with Travic CI

This project provides a first sample travis configuration file for automated builds of RTEMS toolchain.

## Approach

Use travis to fetch Dockerfile for RTEMS toolchain build from github. Use `TARGET_ARCH` to later setup independent builds for the available RTEMS targets. To avoid duplicating similar files, Dockerfile and build scripts have been placed to separate git repositories. The actual RTEMS target can then be controlled by just editing `.travis.yaml` and updating variable `TARGET_ARCH`.

## Current issues

I'm still working on that. Currently, I wasn't able to fully test `.travis.yaml` file with `travis-ci.org` since they don't allow downloads of all the GCC components which is reasonable, at least for the free offer.

