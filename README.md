# SwarmDock ver0.2


SwarmDock is the prebuilt binary distribution of the SwarmPlug system.

SwarmPlug defines the underlying versioned infrastructure and canonical naming model for heterogeneous ROS-based systems.

SwarmDock provides a ready-to-run binary package for ROS1 discovery, host binding, and canonical resource listing.

## Features


- ROS1 Master discovery
- ROS host binding helper
- ROS topic / node / service / parameter listing
- Canonical resource naming
- Prebuilt binary distribution

Canonical output format:

```text
/sp/<host_id>/<kind>/<ros_path>
```

## Download

Please download the prebuilt package from the GitHub Releases page.

Current package:

```text
swarmdock_ver0.2_delivery_x86_64_*.tar.gz
```

## Install

```bash
tar -xzf swarmdock_ver0.2_delivery_x86_64_*.tar.gz
cd swarmdock_ver0.2
./install.sh ~/swarmdock_ver0.2_runtime

echo 'export PATH="$HOME/swarmdock_ver0.2_runtime/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## Configure

Edit:

```bash
vim ~/swarmdock_ver0.2_runtime/env/device.conf
```

Example:

```bash
export SP_NODE_ID=sd-001
export SP_HOST_ID=host-001
export PREFER_IP=192.168.31.133
export SUBNET_PREFIX=192.168.31
```

## Usage

```bash
swarmdock host info
swarmdock --auto topics
swarmdock --auto topics --canon
swarmdock --auto nodes --canon
swarmdock --auto services --canon
swarmdock --auto params --canon
```

## Notes

This public repository provides prebuilt binary releases only.

Source code is not included in the public release package.

## License

This software is distributed as a prebuilt binary package.  
See `LICENSE.txt` for usage restrictions.
# swarmdock-release
