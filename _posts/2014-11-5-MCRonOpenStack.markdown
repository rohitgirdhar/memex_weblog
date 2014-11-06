---
layout: post
title:  "Setting up Matlab Compiler Runtime on memex openstack"
categories: update
---

## Installation
1. Download the relevant MCR (relevant to platform the code is compiled in) from 
the [website](http://www.mathworks.com/products/compiler/mcr/). Unzip in the NFS directory. (The VMs are 64bit).
2. To install,

```bash
$ ./install -destinationFolder /exports/cyclops/software/matlab/MatlabCompilerRuntime -mode silent -agreeToLicense yes
# set the environment variables in /exports/cyclops/software/matlab/MatlabCompilerRuntime/v81/add_env.sh
```

Now MCR is installed in `/exports/cyclops/software/matlab/MatlabCompilerRuntime`.

