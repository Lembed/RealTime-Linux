## linux

```bash
wget https://www.kernel.org/pub/linux/kernel/v4.x/linux-4.8.tar.xz
wget https://www.kernel.org/pub/linux/kernel/projects/rt/4.8/patch-4.8-rt1.patch.xz
xz -cd linux-4.8.tar.xz | tar xvf -
cd linux-4.8
xzcat ../patch-4.8-rt1.patch.xz | patch -p1
```
## sample
collections of RT application samples

## tools
Docker image with linaro gcc cross compiler can used to build real time linux and samples

