# Linux-iPhone-6s-X-howto

This project provides a guide and the necessary tools to boot Linux on compatible iPhones (6s, 6s Plus, 7, 7 Plus, 8, 8 Plus, and X — A9, A10, and A11 devices) on iOS 12-14.5 using checkra1n, pongoOS, and custom kernel images.

## Supported Devices

- iPhone 6s / 6s Plus (A9)
- iPhone 7 / 7 Plus (A10)
- iPhone 8 / 8 Plus / X (A11)

## Prerequisites

- A compatible iPhone (see above)
- A computer running Linux (recommended)
- Administrative rights (`sudo`)
- Required dependencies (`python3`, `git`, `pyusb` and other basic tools)

## Installation

Clone this repository:

```bash
git clone https://github.com/A11pwnX/Linux-iPhone-6s-X-howto.git
cd Linux-iPhone-6s-X-howto
```

## Booting Linux on your iPhone

1. **Launch checkra1n with PongoOS:**

   ```bash
   sudo ./bin/checkra1n -cpk ./pongo/Pongo.bin
   ```

   > This will boot pongoOS on your device.

2. **Load the Linux kernel, DTB, and initramfs:**

   ```bash
   sudo python3 ./bin/load_linux.py -k ./kernel/Image.lzma -d ./kernel/dtbpack -r ./initramfs/initramfs
   ```

   > This command uploads the Linux kernel, dtbpack, and initramfs to your device via PongoOS.

## Project Structure

- `bin/` : Contains the required executables (`checkra1n`, scripts, etc.)
- `pongo/` : PongoOS image (`Pongo.bin`)
- `kernel/` : Kernel image (`Image.lzma`) and dtbpack (`dtbpack`)
- `initramfs/` : Linux ramdisk files (`initramfs`)

## Warnings

- **Use at your own risk!** Do this on your device may cause data loss or damage.
- This project is for experimentation and learning purposes only.

## Credits
https://github.com/konradybcio/linux-apple
https://github.com/konradybcio/pongoOS
https://github.com/SoMainline/linux-apple-resources
https://checkra.in

---

**good luck!**
