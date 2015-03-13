# qemu-binaries
QEMU Binaries for the Pebble emulator

## Building QEMU Binaries

You should be able to follow the instructions on the [Software Tools - QEMU](https://pebbletechnology.atlassian.net/wiki/display/DEV/Software+Tools+QEMU) section of the wiki.

The following sections give you the specific cofigure flags for each platform.

## Building QEMU Binaries for Mac

```
../configure --source-path=.. --extra-ldflags=-g --with-coroutine=gthread --enable-cocoa --enable-debug --disable-werror --target-list="arm-softmmu" --extra-cflags=-DSTM32_UART_NO_BAUD_DELAY --disable-gtk --disable-vnc --disable-debug-info --disable-virtfs --disable-xen --disable-brlapi --disable-vte --disable-debug-tcg --disable-tpm --disable-vhdx --disable-kvm --disable-guest-base --disable-curses --audio-drv-list= --disable-glx --disable-guest-agent --disable-vhost-scsi --disable-vhost-net --disable-quorum --disable-attr --disable-libiscsi --disable-rbd --disable-glusterfs --disable-libusb --disable-usb-redir --disable-smartcard-nss --disable-libnfs --disable-virtfs --disable-rdma --disable-libssh2 --disable-mouse
```

> This assumes you're running configure from a `build` folder inside the `qemu` root directory.

## Building QEMU Binaries for Linux (64 & 32 Bit)

```
../configure --source-path=.. --extra-ldflags=-g --with-coroutine=gthread --enable-cocoa --enable-debug --disable-werror --target-list="arm-softmmu" --extra-cflags=-DSTM32_UART_NO_BAUD_DELAY --disable-mouse
```

> This assumes you're running configure from a `build` folder inside the `qemu` root directory.

