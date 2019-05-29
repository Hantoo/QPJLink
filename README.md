# QPJLink
PJLink Plugin For Qlab

To get started. Please download "[QPJLink.zip](/QPJLink.zip)". This file contains all scripts and a sample QLab file to get you started!

QPJLink is a  easy to use script to allow for use of PJLink from Qlab.
Based of off [DaveTHW's PJLink Script](https://github.com/DaveThw/PJLink), QPJLink expands on the functionality and ease of use of the script.
The Syntax of use is similar of that of [Alec's QSpotify](https://github.com/sparks-alec/QSpotify) in that there is a configuration cue list, as well as the actions are determined by the name of the cue.
This script works no matter how many projectors you have in your setup.

## Configuration

![Configuration Setup](/ReadMe-Assets/ConfigImage.png)
  
When you open the sample QLAB file, there is a cue list called "PJLink Config". 
This cue list contains all the infomation needed to be inputted to make QPJLink work.
Cue "PJLinkScriptDest" should point to the destination in which you store the QPJLink.scpt file. The projector.sh file is to stay in the same folder as the QPJLink.scpt, otherwise the commands will not work.
Each projector can have its own IP stated here. If you need to add more projectors then the cue Number format should follow as:

    PJLinkIP_Projector[Number]
    
and the IP of the projector entered into the cue name.
You can put as many projectors here as you like. Ensure you enter the correct IPV4 address for each projector. Entering the incorrect projector IP will cause PJLink to hang while it tries to connect to the non-existant projector.

After entering in all this infomation you are ready to setup your cues!

## Cues

![Cues Setup](/ReadMe-Assets/SettingUpCues.png)

You can only use script cues to control QPJLink. It is recommended that you copy and paste the cues from the sample QLAB4 file to your own file (along with the PJLink Config Cuelist).
As mentioned above, the syntax of the cues have been created similar to that of Qspotify so that it is easier for people to grasp.
An example cue is: "PJLink:Projector1:Power Off"
where

    PJLink:Projector[number]:[command]
    
You can write any notes before PJLink to help you understand this que. Please do not write "PJLink" in the notes before the "PJLink:Projector...." section otherwise the script will get confused. The script looks for the PJLink in the cue name.

## Support Commands
Currently the only supported commands are:
* "Power On"
* "Power Off"
* "Shutter Open"
* "Shutter Close"

More commands are looking to be added in the future.

##Troubleshooting

If the terminal show permission denied for projector.sh file then run
    
    chmod +x ~/Desktop/QPJLink/Scripts/Projector.sh

