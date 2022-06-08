# README #

### What is this repository for? ###

This repo supports tools that extend regular LXC utilities.  These extensions provide container maintenance, specific to my development environment and style, including:

* Automatic start or unfreeze of containers before the intended operation begins (rather than throwing an error because a container is stopped or frozen -- yes, a pet peeve!)
* Support for a foreign 'build' container so that build tools can be installed in one place, while built images can be imported into the local container (freeing up space for many containers)
* Batch operations for all containers (in unison)
* Easy LXC environment set up and configuration
* Bash completion support

### What's included? ###

The following tools are included:

* **lxc-all** - Operate on all containers, including
    * Start all
    * Stop all
    * Freeze all
    * Unfreeze all
    * Upgrade all
* **lxc-build** - Create or upgrade a container (optional: regular user added, SSH added)
    * Build applications using a foreign 'build' container
    * Install built images into the local container
    * (Requires initially building a container named 'build' with build tools)
* **lxc-rsync** - Transfer files and/or directories
    * From the host into a container
    * From a container to the host filesystem
* **lxc-setup** - Effect container-specific or system-level settings, including
    * Show container status
    * Toggle auto-start for container
    * Destroy (stop and remove) container
    * Show LXC system configuration
    * Enable unprivileged containers
    * Enable user-based auto-start
* **lxc-sh** - Connect to container via shell access
    * Ensures container is running
    * Attaches to container as root[default] or regular user

### But why? ###

I run a few dozen containers at once, so as to

* Emulate harware devices
* Accelerate application development
* Load-test applications using several containers, applying stress to a single target container

These tools help accelerate the build and test processes.

