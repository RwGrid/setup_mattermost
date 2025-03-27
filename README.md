# setup_mattermost

<h1>Steps to install mattermost:</h>
<p>
 <ul>
  <li>install mattermost with https with a domain given by client</li>
  link: https://docs.mattermost.com/install/install-docker.html
  <li>copy directory https://github.com/mattermost/docker into the ubuntu machine</li>
  <li>then perform steps in tutorial</li>
  <li>change the .env file domain to ur domain</li>
  <li>install with nginx to prevent port in domain name and VOILA</li> </ul> </p>
---------------------------------------------------------------------------
<h2>How to install plugins</h2>
  installing the focal board plugin
  1-this is the directory of bind mount volume of docker, as you see here
  /home/docker/volumes/app/mattermost/client/plugins
  2-cd into directory 
  3-wget  from here https://github.com/mattermost/mattermost-plugin-boards/releases, do not use the old one , use 9.1 , rename boards to focalboard
  4- tar -xvf ./plugin.tar.gz
  increase max file size in config.json and allow plugin upload in config.json
  /home/docker/volumes/app/mattermost/config
  in file settings header, maxfilesize
  and in plugins, allow plugins
  5-update the config to allow the plugin to true 
  6- in WEB UI, enable the plugin, it will show problem of icon
  go to all directories inside the /home/docker/volumes/app/mattermost/client/plugins/focalboard
  and perform chmod -R O+rw ./directories 
also install the github, call and voice from market place, but they are easy
call limit is 1 on 1 
