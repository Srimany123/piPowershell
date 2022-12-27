<h1 align="center">Powershell installation in Raspberry Pi</h1>
<i>As we know powershell is no less crucial shell terminal than any popular terminal. people who know the pros of powershell crave for its usage. se hence the installation</i>

<h2>Automated installation</h2>
  
if you are using this repository for installation. copy the following commands
  
<div>
  <pre>
    cd ~
    sudo git clone https://github.com/Srimany123/piPowershell.git
    cd piPowershell</pre>
  
  if you want audio acknowledgement of key installation names and updates of progress, then use this command : 
  
  <pre>
    bash start -sd</pre>
  else if you don't want know those details and just want to complete the installation then us this command:
  <pre>
    bash start</pre>
</div>
<p>Wait a few minutes and the installtion will be automatically completed
</p>
<p>After this we pretty much done. now just type the following given command anywhere in the terminal to open the powershell.
</p>
  <pre>
    pwsh</pre>
<b>Optional step :</b>
<p>As we can be very forgetful i just created little OpenPWSH.sh script to keep reminding even when you offline. trust me forgetting happens alot.</p>
  <pre>
    ./OpenPWSH.sh</pre>

<h2>Manual installation</h2>

To begin with manual installation

<div>
  for any kind installation first we have to update the linux environment and then upgrade it to latest rolling.
  
  <pre>
    sudo apt update && sudo apt upgrade</pre>
  after we completed upgrading, Now we need to install some necessary libraries.
  <pre>
    sudo apt install wget libssl1.1 libunwind8</pre>
  Neede libraries are installed. Now we give executable permissions.
    sudo chmod +x *
  We are going to make a directory at opt/microsoft/powershell/7
  <pre>
    sudo mkdir -p /opt/microsoft/powershell/7</pre>
  By this we are ready to install image, here we have to install the correct image which is used for system, if the system is 64 bit use the foloowing commands to download the image.
  <pre>
    wget -O /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v7.2.6/powershell-7.2.6-linux-arm64.tar.gz</pre>
else if the system is 32 bit then use this command to install.
  <pre>
    wget -O /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v7.2.6/powershell-7.2.6-linux-arm32.tar.gz</pre> 
  By far we have downloaded and steup the environment, now we need to extract the image file.
  <pre>
    sudo tar zxf /tmp/powershell.tar.gz -C /opt/microsoft/powershell/7</pre>
  After the extraction we have to give it executable permission
  <pre>
    sudo chmod +x /opt/microsoft/powershell/7/pwsh</pre>
  After this we are good to go. But wait, we are in fast world where everything is in rush. we don't got time to remember or goto this directory everytime and execute the 'pwsh'. so we simply use the ln -s to link the word to use it from anywhere by simply typing 'pwsh' in anywhere. to do that we use the following command
  <pre>
    sudo ln -s /opt/microsoft/powershell/7/pwsh /usr/bin/pwsh</pre>
  We are done with the total process so we don't actually have no use of the powershell image file. Also space is something which is very crucial in mini computers or virtual devices. so my preferred choice is to remove the powershell image file as it is no longer useful."
  <pre>
    sudo rm -rf /tmp/powershell.tar.gz</pre>
</div>
if you encounter any errors, mail me.

<b>Email :</b> <i>yalavarthisreeman21725@gmail.com</i>
