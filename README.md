# setup-dataiku

from https://www.dataiku.com/product/get-started/linux/

<ol>
  <li>Download DSS</li>
  wget https://cdn.downloads.dataiku.com/public/dss/11.3.2/dataiku-dss-11.3.2.tar.gz

  Or, use this direct link.
  DSS works on Ubuntu, Debian, CentOS, RHEL and Amazon Linux. For version details, please see our Requirements page.
  
  <li>Unpack</li>
  Unpack the downloaded archive where you want to install DSS.
  You must keep the directory even after installation is complete.

  tar xzf dataiku-dss-11.3.2.tar.gz

  <li>Install</li>
  Launch the installation script. You need to choose:
  <ul>
    <li>A directory where Dataiku DSS will store configuration and data.</li>
    <li>A base TCP port.</li>
  </ul>
  dataiku-dss-11.3.2/installer.sh -d DATA_DIR -p 11000

  <li>Start</li>
  DATA_DIR/bin/dss start

  <li>Enter the studio</li>
  Browse to http://your_server_address:11000

  <li>Configure crontab to restart dataiku on reboot</li>
  crontab -e
  @reboot cd /home/dave && bin/dss start

</ol>
