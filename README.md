# open_robotics_embedded
Drive motor and turntable controller for OpenRobotics.ca<br>

Seriously any questions get at me max@theprogrammingclub.com<br>
<br>
<u>Things you need to be effective here:</u><br>
git:<br>
  <a href="https://windows.github.com/">Windows install</a><br>
  <a href="http://git-scm.com/download/linux">Linux/Unix install</a><br>
Our Trello page:<br>
  https://trello.com/openrobotics
Slack is helpful:<br>
  https://opbots.slack.com/<br>
<br>
<u>About the repo</u><br>
We program in a mix of Arduino and CPP over USB and using ICSP, usually using avrdude.exe to program<br>
http://www.atmel.com/microsite/atmel_studio6 is used as a dev environment with the Visual Micro extension<br>
For serial programming in a non-Arduino project:<br>
&nbsp;&nbsp;Select Tools -> External tools<br>
&nbsp;&nbsp;&nbsp;&nbsp;Choose Add<br>
&nbsp;&nbsp;&nbsp;&nbsp;Set Title to 'Serial Program'<br>
&nbsp;&nbsp;&nbsp;&nbsp;Change the command to your Arduino directory that includes avrdude<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: <code>C:\Program Files (x86)\Arduino\hardware\tools\avr\bin\avrdude.exe</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;Change the Arguments to match your situation, replacing COM16 with the COM port you are using
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: <code>-C"C:\Program Files (x86)\Arduino\hardware\tools\avr\etc\avrdude.conf" -patmega328p -carduino -P\\.\COM16 -b57600 -U flash:w:"$(ProjectDir)Debug\$(ItemFileName).hex":i -v</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;Click ok<br>
&nbsp;&nbsp;&nbsp;&nbsp;Now to program, select Tools -> Serial Program<br>
<br>
Email me! max@theprogrammingclub.com<br>
I want to make this documentation effective<br>
<br>
Git workflow: <br>
<code>  git pull origin master</code><br>
<code>  [do your stuff]</code><br>
<code>  git add [new files]</code><br>
<code>  git pull origin master</code><br>
<code>  git commit -am "[commit message]"</code><br>
<code>  git push origin master</code><br>
<br>
In case of Git conflicts: <br>
<code>git checkout -b [some name that indicates this branch is screwed up]
&nbsp;&nbsp;Initiate a pull request on github.com