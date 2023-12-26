# setup-dataiku

from https://www.dataiku.com/product/get-started/linux/

<ol>
  
  <li>Download DSS</li>
  <ul>
    <li>wget https://cdn.downloads.dataiku.com/public/dss/11.3.2/dataiku-dss-11.3.2.tar.gz</ul>
    <li>DSS works on Ubuntu, Debian, CentOS, RHEL and Amazon Linux.</li>
    <li>For version details, please see our Requirements page.</li>
  </ul>
  
  <li>Unpack</li>
  <ul>
    <li>Unpack the downloaded archive where you want to install DSS.</li>
    <li>You must keep the directory even after installation is complete.</li>
    <li>tar xzf dataiku-dss-11.3.2.tar.gz</li>
  </ul>

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
  <ul>
    <li>crontab -e</li>
    <li>@reboot cd /home/dave && bin/dss start</li>
  </ul>

</ol>
