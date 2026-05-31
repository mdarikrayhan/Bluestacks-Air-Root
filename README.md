# Root BlueStacks Air macOS

## Tested on BlueStacks Air

- 5.21.680.7532
- 5.21.695.7506
- 5.21.700.7523
- 5.21.705.7515
- 5.21.712.7503
- 5.21.715.7538
- 5.21.720.7530
- 5.21.730.7536
- 5.21.735.7518
- 5.21.745.7536
- 5.21.770.7524

![Screenshot](/images/bluestacks-air-root-magisk.png)

## Requirements

- [BlueStacks Air](https://www.bluestacks.com/mac)  
  Direct download (bundled in this repo, Git LFS): [BlueStacksInstaller 5.21.770.7524](https://github.com/mdarikrayhan/Bluestacks-Air-Root/raw/main/BlueStacksInstaller_5.21.770.7524_37bb8a3d74002edaa7c7084b8a7648f6.pkg)
- Kitsune Magisk (tested version: v27.2-kitsune-4)  
  Direct download (bundled in this repo): [magisk.apk](https://github.com/mdarikrayhan/Bluestacks-Air-Root/raw/main/magisk.apk)

## Rooting

- Install BlueStacks Air ([download bundled installer 5.21.770.7524](https://github.com/mdarikrayhan/Bluestacks-Air-Root/raw/main/BlueStacksInstaller_5.21.770.7524_37bb8a3d74002edaa7c7084b8a7648f6.pkg))
- ‼️ **REQUIRED** ‼️ Open BlueStacks Air for the first time
- Close BlueStacks Air
- Download this repo and extract it
- The `magisk.apk` (Kitsune Mask) is already included in the repo. To use a different version, replace `magisk.apk` in the project folder
- Open **Terminal.app** or **iTerm.app** and navigate to the project folder

  ```bash
  cd ~/Downloads/root-bluestacks-air
  ```

### Method 1: SIP enabled

- Execute `root.sh` specifying initrd output path and backup directory

  ```bash
  bash root.sh -o files/initrd_hvf.img -b files/backup
  ```

  the above command will backup the original `initrd_hvf.img` in `files/backup` and create a patched one in `files/initrd_hvf.img`, you may specify a different path for the output and backup directory
- Copy the patched `initrd_hvf.img` to `/Applications/BlueStacks.app/Contents/img/` and replace the original one
- Start BlueStacks Air
- Continue with [Next Steps](#next-steps)

### Method 2: SIP disabled

- Execute `root.sh` with sudo

  ```bash
  sudo bash root.sh
  ```

- Wait until BlueStacks Air starts
- Continue with [Next Steps](#next-steps)

### Next Steps

- Install Kitsune Mask (`magisk.apk`)
- Open Kitsune Mask and press **OK** when the **Requires Additional Setup** prompt appears. This will reboot BlueStacks Air.
  ![magisk-additional-setup](/images/magisk-additional-setup.png)
- Force quit BlueStacks Air if necessary
- Open BlueStacks Air and enjoy
- If you need **Zygisk**, enable it from Kitsune Mask settings and reboot BlueStacks Air

## Unrooting

### Method 1: SIP enabled

- Copy the backup `initrd_hvf.img` to `/Applications/BlueStacks.app/Contents/img/`
- Done

### Method 2: SIP disabled

- Make sure BlueStacks Air is closed
- Execute `unroot.sh` with sudo

  ```bash
  sudo bash unroot.sh
  ```

- Done
