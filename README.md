# Virt-Man-Win-Files

This is a guide on how to setup a Win-Client in Virt-Manager


## Resources
 - WinFS => A Service which enables the function to access host directories https://winfsp.dev/rel/
 - VirtIO => Package for Ethernet-Adapters and also needed for WinFS https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso

## Steps
 1. If you dont have an internet connection you can share the files by enabling and disabling a USB-Stick (remember to dismount)
 2. Execute the .msi-File from WinFS and just click next through
 3. Execute the x64.msi-File from VirtIO by just using the VirtIO-Iso as a Directory
 4. Keep the Directory Open so that ther is a cd-disk in you file manager
 5. So now we are enabling the WINFS-Service
     1. Enter the Services-App
     2. Search for VirtIO-FS and start it and enable auto-start
 6. If you have problems with the Internet card go to the Device-Manager
 7. If you have a RedHat Adapter with an attention sign then delete the Device and check to delete the driver too
 8. Now refresh the page
 9. Search for an "Ethernet Controller"
 10. Update Driver
 11. Now choose the CD-Disk we opened before and choose NetKVM/<windows-version>/<architecture>
 12. If the same Adapter appears again with a attention symbol than repeat 7-11

## Links and Other Explanations
- https://pve.proxmox.com/wiki/Windows_VirtIO_Drivers (Proxmox)
- https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF#Virtio_network (Arch Community)
- https://superuser.com/questions/1671932/unable-to-connect-to-internet-in-windows-10-vm-using-kvm-qemu (Stack Exchange)
