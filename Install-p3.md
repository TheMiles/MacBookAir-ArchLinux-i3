[Previous Page](/Install-p2.md)
<h1 align="center"> Part III - Hardware Setup + GUI Extras</h1>

1. Bluetooth Support

   ```shell
   $ sudo pacman -S blueman ell
   ```

- Enable Service:

  ```shell
   $ sudo systemctl enable --now blueman-mechanism
  ```

2. Wireless Support

   ```shell
   $ sudo pacman -S dkms broadcom-wl-dkms
   
   $ sudo reboot
   ```
3. Webcam Support

   ```shell
   $ paru -S facetimehd-firmware facetimehd-dkms facetimehd-data
   $ sudo reboot
   ```
4. Keyboard light

   ```shell
   $ paru -S kbdlight macbook-lighter
   
   $ sudo systemctl enable --now macbook-lighter
   ```

5. plymouth

   ```shell
   $ paru -S plymouth
   $ nano /etc/mkinitcpio.conf
   ```
    - add HOOKS=(....udev plymouth...)
 
   ```shell
   $ sudo nano /boot/loader/entries/arch-zen.conf
   ```  
 
    - add `quiet splash vt.global_cursor_default=0` to the end of the last line 
 
   ```shell
   $ sudo mkinitcpio -P
   $ reboot
   ```
