#!/bin/bash
mnt_point="/mnt/repair_kindle_code_2"
last_drive=$(lsblk  -n -p -l | grep "disk" | awk '{print $1}' | tail -n 1)
next=0
for i in "/dev/sd"{a..z}
	do if [ "$next" -eq 1 ]
then kindle_device="$i"1
	break
fi
if [[ "$i" = "$last_drive" ]]
then next=1
fi
done

mkdir "$mnt_point" || umount "$mnt_point"

until [ -b "$kindle_device" ] 
do sleep 0.05
done

mount "$kindle_device" "$mnt_point"
touch "$mnt_point"/DO_FACTORY_RESET
umount "$kindle_device"
rm -d "$mnt_point"

echo "Done! Restart your kindle, it should do factory reset and turn on as a resh device."
