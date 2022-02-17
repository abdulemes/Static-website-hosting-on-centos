Step 1 - Create a directory named vagrant-vms
  
  Command: mkdir vagrant-vms

Step 2 - Create a directory with the name of the website to be hosted.
  
  Comman: mkdir wavecafe

Step 3 - Change directory to the directory created in step 2
 
 Command: cd wavecafe

Step 4 - Create a vagrantfile in the wavecafe directory with the vagrant box config gotten from vagrant cloud.
 
 Command: vagrant init <Virtual box link>

  ![IMG_8943](https://user-images.githubusercontent.com/93732510/154569961-9c22f576-9000-45b7-8be8-8a3cd31b21c4.jpg)

Step 5 - Use vim editor to modify the vagrantfile configuration. (this is to enable IP the address)

Step 6 - Bring up the vm 
 
  Command: vagrant up

  ![IMG_8944](https://user-images.githubusercontent.com/93732510/154570408-2e2c90df-2e42-4c10-83f0-c959ac961fae.jpg)

Step 7 - Now that the vm is running, we can log into it. 
 
  Command: vagrant ssh
  
Step 8 - Change to root user
  
  Command: sudo -i
 
Step 9 - Install httpd
 
  Command: yum install httpd wget unzip -y
  
  ![IMG_8946](https://user-images.githubusercontent.com/93732510/154574623-a80538e0-94ed-45eb-a89d-fe8120d472ea.jpg)

Step 10 - Start the server and also enable the server.
 
  Command: systemctl start httpd 
  
  Command: systemctl enable httpd
  
  ![IMG_8947](https://user-images.githubusercontent.com/93732510/154574692-05be9d68-67ad-4369-a1df-196916b31548.jpg)

Step 11 - Access the default server page. Use ifconfig or IP addr show command to look up the IP address
  
  ![IMG_8948](https://user-images.githubusercontent.com/93732510/154575410-940fd02b-825b-40c0-8134-fd0e3f7e8cde.jpg)
  
Step 12 - Change directory to the default web directory path
   
  Command: cd /var/www/html
  
Step 13 - Create an html.text inside the directory using Vi editor
   
  Command: vi index.html
 
Step 14 - Restart the server to check the newly written html text created in the vi editor
    
  ![IMG_8949](https://user-images.githubusercontent.com/93732510/154576565-32605eb2-d2fe-46c7-9db9-b15220b5f267.jpg)

Step 15 - Copy the download link from tooplate.com using F12 button on the keyboard, navigate to network tab to copy the link. 
  
Step 16 - Change directory to temporary so as to paste the link there.
   
  Command: cd /tmp

Step 17 - In the temporary directory, type wget + the copied link from step 16
  
  ![IMG_8951](https://user-images.githubusercontent.com/93732510/154581028-a687a3f7-cee4-46dc-9bb1-f135cd81eb39.jpg)

  
Step 18 - unzip the downloaded link 
  
  Command: unzip 2121_wavecafe.zip
  
  ![IMG_8952](https://user-images.githubusercontent.com/93732510/154581134-9ce54aed-5850-4a8c-b20c-cfe3d29a35a5.jpg)

  
Step 19 - Chnage directory to 2121_wave_cafe
 
Step 20 - Copy into web directory 
 
  Command: cp -r * /var/www/html
  
Step 21 - Restart the server and check the status

  Command: systemctl restart httpd
  
  Command: systemctl status httpd
  
  ![IMG_8953](https://user-images.githubusercontent.com/93732510/154581788-72f42eac-735f-4c48-b70b-d3fc04ec7207.jpg)

Step 22 - Refresh the safari browser to see the website displayed. 
  
  ![IMG_8954](https://user-images.githubusercontent.com/93732510/154582120-da15c556-efe1-4d44-99e4-b7a24f9ad655.jpg)
