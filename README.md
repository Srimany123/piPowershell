<h1 align="center">Powershell installation in Raspberry Pi</h1>
<i>As we know powershell is no less crucial shell terminal than any popular terminal. people who know the pros of powershell crave for its usage. se hence the installation</i>

<h2>Automated installation</h2>
  
if you are using this repository for installation. copy the following commands
  
<div>
  <pre>
    cd ~
    sudo git clone https://github.com/Srimany123/piPoershell.git</pre>
  
  if you want audio acknowledgement of key installation names and updates of progress, then use this command : 
  
  <pre>
    bash start -sd</pre>
  else if you don't want know those details and just want to complete the installation then us this command:
  <pre>
    bash start</pre>
</div>
<p>wait a few minutes and the installtion will be automatically completed
</p>

<h2>Manual installation</h2>

To begin with manual installation

<div>
  for any kind installation first we have to update the linux environment and then upgrade it to latest rolling.
  
  <pre>
    sudo apt update && sudo apt upgrade</pre>
  after we completed upgrading,
  <pre>
    sudo apt install wget libssl1.1 libunwind8
    sudo chmod +x *
    sudo mkdir -p /opt/microsoft/powershell/7
    echo "incase of 64 bit un comment the arm64 and comment the arm32."
    wget -O /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v7.2.6/powershell-7.2.6-linux-arm32.tar.gz 
    #wget -O /tmp/powershell.tar.gz https://github.com/PowerShell/PowerShell/releases/download/v7.2.6/powershell-7.2.6-linux-arm64.tar.gz 
    sudo tar zxf /tmp/powershell.tar.gz -C /opt/microsoft/powershell/7
    sudo chmod +x /opt/microsoft/powershell/7/pwsh
    sudo ln -s /opt/microsoft/powershell/7/pwsh /usr/bin/pwsh
    sudo rm -rf /tmp/powershell.tar.gz
</div>
