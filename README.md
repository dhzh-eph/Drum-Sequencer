# Drum-Sequencer
## Analog circuit of a drum sequencer, heavily inspired by Erica Synths and Moritz Klein DIY Drum Sequencer

<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/8d3e95e4-e359-4663-b667-ac1a2f6d115d" /> Solder Stand <br/>
We will be using this "helping hand magnifier led light with soldering stand" to help us with holding the pcb during soldering. <br/>
https://www.youtube.com/watch?v=MabbxcKlfss reference on how to build the stand.

##### Materials List
Before starting soldering, ensure you have the following: <br/>
Solder (ideally lead free) <br/>
Soldering Iron <br/>
Flux (rosin or resin, ideally liquid to prevent waste and easier soldering) <br/>
Fumehood (most ideal) <br/>
Tip Tinner Cleaner <br/>
Copper Coated Sponge <br/>

Most of these can be bought from Amazon, AliExpress or any other site. The tools being used would look like the following below.
<img width="1200" height="800" alt="test" src="https://github.com/user-attachments/assets/b5795099-1f47-4b8f-80bf-63cf9104754e" /> <br/>

##### What are the components in the list used for?
First, the soldering iron and solder are essentially our glue gun and glue stick. The soldering iron is used to melt solder, and the solder is used to help components "stick" to the pcb. As for flux, it allows for solder to flow and stick to the copper pads of the pcb. How it works is...

For the fumehood, it extracts the fumes that are emitted during the melting of solder. Even though lead-free solder is less harmful than full lead, the fumes are still harmful to breathe in, so it's ideal to solder in a well ventilated place with a fumehood to pull the fumes away from you. The tip tinner is used to remove the soldering iron tip of all artifacts and debris. This allows for the fresh solder to

##### Why lead-free solder over full leaded solder?
Full leaded solder is actually fine, and more ideal for most cases of soldering. However, it is harmful to hold full leaded solder for a long duration of time, and there may be side effects from doing this. If you are working in a ventilated area with professional equipment, then leaded solder is preferred. This is because leaded solder takes a lower temperature to melt, and flows a lot more smoothly to copper pads when implemented with flux.

When  soldering, ensure that the temperatures and time duration you use the soldering iron for is within recommended conditions. For example, some soldering iron tips have a recommended temperature range of up to 300 degrees Celsius. If this is exceeded, the tip will either melt or start to oxidize, melting making it much harder to get proper solder onto a PCB, and oxidizing making it very difficult to get solder onto the iron tip.<br/>
Oxidizing may also permanently damage the tip to the point that solder will not stick to the tip. In the case you're a beginner like me, buy a few extra tips to ensure smooth learning and timeline development for your projects.

In the case that your tip oxidizes, be sure to set the heating temperature within recommended conditions, and to clean it using tip tinner cleaner and copper coated sponge. 

<img width="1000" height="1250" alt="IMG_3746" src="https://github.com/user-attachments/assets/eb95ca61-e6ea-493a-bc4f-958bc96b4e91" />
<img width="1250" height="1000" alt="IMG_3745" src="https://github.com/user-attachments/assets/f62d983c-8c03-427a-8b92-ace94ba4ff6b" /> </br>
After soldering it should look something like this. Unfortunately one of the four pins is heavily scratched due to accidental large amounts of solder originally sicking to 3 of the pins. I had to manually scrap it to get it off as the solder wasn't melting regardless of using flux, different temperatures and other tools. Also, note that here I've applied too much flux, which makes it very messy. Note to self to apply less resin.

Here, we now need to repair the traces, and we also need to re-add the solder mask, and do continuity tests with a multi meter to check for signal integrity. As such, copper wires are needed. The repair itself is fairly straightforward, using a 

Note to self, definitely stick the breadboard onto the pcb first before soldering the female pin heads to the pcb. Otherwise it's very easy to have it misalign (also not really possible to unstick the breadboard once its touching the pcb).
<img width="1000" height="1250" alt="IMG_3763" src="https://github.com/user-attachments/assets/bfbc8c44-55dd-4690-a36f-aaf0e8b0f1b9" />




