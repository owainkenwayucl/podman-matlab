# podman-matlab
This repo contains podman `Dockerfile`s for running Matlab in various places.

* `local-file` - Build a container based on AlmaLinux 10.x and a user-provided `matlab.tar.gz` file which should include license settings.
* `mpm` - Build a container based on AlmaLinux 10.x and the `mpm` package manager. Provide a `network.lic` file.

To build, fulfil any requirements (e.g. obtaining a `matlab.tar.gz` and placing it in the right directory and do something like:

`build -t matlab:r2025b .`
