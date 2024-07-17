# 下载工具
``` 
$ brew tap riscv/riscv
$ brew install riscv-tools
brew install qemu 
```
# 测试工具
xv6源码目录下终端输入
```
make qemu
```
输出
```
qemu-system-riscv64 -machine virt -bios none -kernel kernel/kernel -m 128M -smp 3 -nographic -global virtio-mmio.force-legacy=false -drive file=fs.img,if=none,format=raw,id=x0 -device virtio-blk-device,drive=x0,bus=virtio-mmio-bus.0

xv6 kernel is booting

hart 1 starting
hart 2 starting
init: starting sh
$ 

```
