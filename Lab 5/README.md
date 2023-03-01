1-dd if=/dev/zero of=/tmp/file1.img bs=512 count=40000

2-losetup -f
  sudo losetup -P /dev/loop6 /tmp/file1.img

3-sudo fdisk /dev/loop6
  n
  w

4-sudo mkfs.ext4 /tmp/file1.img
  y

5-sudo mount /dev/loop6 /mnt


6-cd /mnt
  sudo touch file2.txt

7-sudo apt search gparted
  sudo apt install gparted

8- sudo gparted /dev/loop6

<br>
![1](https://user-images.githubusercontent.com/122295277/222158256-69422ed9-0f95-4eca-9981-0337bd22c600.png)
<br>
![2](https://user-images.githubusercontent.com/122295277/222158269-bd454ef7-39c2-4af3-a4ae-5817016a0b56.png)
<br>
![3](https://user-images.githubusercontent.com/122295277/222158280-bc9183ae-f686-4571-994f-6b66873bebae.png)
