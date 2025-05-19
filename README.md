# emtop-cm4-et-ind
this is for emtop industial mother board on raspberry pi cm4

## Step1, Downlond dtbo files for the board
git clone https://github.com/EMTOP-TECH/emtop-cm4-et-ind.git
cd emtop-cm4-et-ind
sudo chmod -R a+rwx *
## Step2,Copy dtbo to overlay folder
sudo cp emtop-cm4-et-ind.dtbo /boot/firmware/overlays/
## Step3,add dtbo files to config.txt follow [all]
sudo nano /boot/firmware/config.txt

add below contents last line follow [all]
enable_uart=1
dtoverlay=emtop-cm4-et-ind
dtoverlay=vc4-kms-dsi-7inch
dtoverlay=imx219,cam0
dtoverlay=imx219,cam1


press ctrl+x,save the file and reboot


