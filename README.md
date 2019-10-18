# usbip
playing around with usbip

The server will automaticly bind all USB devices
The client will automaticly connect to the server and mount all USB devices


# server install

  apt-get install usbip
  
  modprobe usbip_host
  
  echo 'usbip_host' >> /etc/modules
   
  -
   
  #place usbipd.service in /lib/systemd/system/
   
  -
  
  sudo systemctl --system daemon-reload
  
  sudo systemctl enable usbipd.service
  
  sudo systemctl start usbipd.service
  
  
  
# client install

  apt-get install usbip
  
  modprobe usbip_host
  
  echo 'vhci-hcd' >> /etc/modules
  
  -
  
  #place usbip.service in /lib/systemd/system/
  
  #place usbip-env in your home folder example: /home/pi/<PLACE HERE>
  
  -
  
  sudo systemctl --system daemon-reload
  
  sudo systemctl enable usbipd.service
  
  sudo systemctl start usbipd.service
  
