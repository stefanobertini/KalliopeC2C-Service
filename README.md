KalliopeC2C-Service
==================

An Automator Service to dial numbers on a <a href="http://www.kalliopepbx.com//">Kalliope PBX</a>

To setup the service you have to:<br>


1) Double click the workflow and select "Install" (or copy the workflow to your ~/Library/Services folder)

2) Double click on the workflow and setup it using these parameters:

SERVER=The http prefix url for your calliope<br>
USERNAME=Your phone's username<br>
PASSWORD=Your phone's password MD5 encoded<br>
TIMEOUT=The connection timeout in seconds<br>
STRIPCHARS=A regular expression array of bad characters to strip from phone numbers<br>
<br>
To create the MD5 encoded password you can type<br>
echo -n 'yourpasswordhere' |  md5<br>
in a shell<br>
<br>

Example<br>
SERVER=http://192.168.43.104<br>
USERNAME=20<br>
PASSWORD=165c3277d601bc93aa053489b12f90cd<br>
TIMEOUT=5<br>
STRIPCHARS=("+39" "[ -//]") <br>
(Removes the Italian country code prefix, spaces and - chars)

Then, to use the plugin, just:<br>
Select a telephone number in any software<br>
Right click with the mouse or open the application's the main menu<br>
Select the "Services" menu<br>
Select "Call with Kalliope"
