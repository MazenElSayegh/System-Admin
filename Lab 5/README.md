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

![1](https://user-images.githubusercontent.com/122295277/222160087-a6dc9cc6-b958-458e-887e-c3d6239a6c2a.png)
![2](https://user-images.githubusercontent.com/122295277/222160116-b97bbc0e-a056-46a0-9806-c94917bb7196.png)
![3](https://user-images.githubusercontent.com/122295277/222160069-9b130665-7673-4803-bc0d-6d35ca5ab564.png)

