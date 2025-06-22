
# Genymotion

## Installation

* Navigate to [Genymotion](https://www.genymotion.com/product-desktop/download/) and download the linux runtime.
* To install the app do the following, the application generally gets installed at `/opt/genymotion` .
```bash
chmod +x genymotion-version-linux_x64.run

sudo ./genymotion-version-linux_x64.run -d
```

## AVD

* To create an `Andorid Virtual Device` we need to login to the community edition of genymotion.
* Since this is gonna be a minimal build lets go with a `custom phone` with api as `11.0-api 30` .
* The no. of processors are gonna be `2` and the `memory size` is gonna be `1024` .


### Mesa errors

* It's common to encounter mesa dri3 virtual driver errors and it can be remediated by installing the drivers first

```bash
sudo apt update && sudo apt upgrade mesa-utils mesa-vulkan-drivers
```

* Then launching genymotion with the dri3 disabled like below.

```bash
LIBGL_DRI3_DISABLE=1 ./genymotion
```

