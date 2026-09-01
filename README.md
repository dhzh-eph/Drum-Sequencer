# Drum-Sequencer
## Analog Drum Sequencer, heavily inspired by Erica Synths and Moritz Klein DIY Drum Sequencer

<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/8d3e95e4-e359-4663-b667-ac1a2f6d115d" /> Solder Stand <br/>
We will be using this to help us with holding the pcb during soldering. <br/>
https://www.youtube.com/watch?v=MabbxcKlfss reference on how to build the stand.

##### What is soldering and why is it important?
Soldering is the concept of gluing components together with conductive metals, examples being operational amplifiers or integrated circuits being soldered to a PCB (printed circuit board). It is important, as it allows for customization of PCB's with different components, and also allows for certain boards to serve specific tasks (examples being AC to DC converters, or specific amplifiers). Compared to a breadboard, the components on a PCB won't be at risk of falling out and requiring setup everytime.

##### Materials List
Before starting, ensure you have the following: <br/>
Solder (lead or lead free) <br/>
Soldering Iron <br/>
Flux (rosin or resin, ideally liquid flux to make soldering easier) <br/>
Fumehood (most ideal for extracting toxic fumes) <br/>
Tip Tinner Cleaner (keeps the tip clean) <br/>
Copper Coated Sponge (removes excess solder) <br/>
99% isopropyl alcohol <br/>

Most of these can be bought from Amazon, AliExpress or other sites. The tools being used would look like the following below.
<img width="1200" height="800" alt="test" src="https://github.com/user-attachments/assets/b5795099-1f47-4b8f-80bf-63cf9104754e" /> <br/>

##### What are the components in the list used for?
The soldering iron, solder, and flux can be viewed as a more complex version of a glue gun and glue stick. The soldering iron is used to melt solder, and the solder is used to connect external components in place on pcb copper pads through thermal bonding with the help of flux. As flux allows solder to actually flow and stick to the copper pads of the pcb, it is required for connections of components.

When solder or copper pads are exposed to air, a small layer of oxidation is formed on top (kind of like rust, but not visible to the human eye). When flux is heated, it chemically reacts and removes the oxidation from the copper pads and componenent leads. This reduces surface tension which allows for the melted solder to flow and wet on the copper pad surface. However, prior to applying flux one should often ensure to apply isopropyl alcohol (ideally 99%) so to remove dust, oil from hands, and to also remove flux residue after soldering as flux is often corrosive/acidic.

For the fumehood, it extracts the fumes that are emitted during the melting of solder. Even though lead-free solder is less harmful than full lead, the fumes are still harmful to breathe in, so it's ideal to solder in a well ventilated place with a fumehood to pull the fumes away from you. The tip tinner is used to remove the soldering iron tip of all artifacts and debris, often being oxidation of flux. This makes it so that solder can adhese to the soldering iron.

##### Why lead-free solder over full leaded solder?
Full leaded solder is actually fine, and more ideal for most cases of soldering. However, it is harmful to hold full leaded solder for a long duration of time, and there may be side effects from doing this. If you are working in a ventilated area with professional equipment, then leaded solder is preferred. This is because leaded solder takes a lower temperature to melt, and flows a lot more smoothly to copper pads when implemented with flux. Otherwise, lead free solder is better as it usually only contains tin and copper/silver which isn't as harmful to your health.

When  soldering, ensure that the temperatures and time duration you use the soldering iron for is within recommended conditions. For example, some soldering iron tips have a recommended temperature range of up to 300 degrees Celsius. If this is exceeded, the tip will either melt or start to oxidize, melting making it much harder to get proper solder onto a PCB, and oxidizing making it very difficult to get solder onto the iron tip.<br/>
Oxidizing may also permanently damage the tip to the point that solder will not stick to the tip. In the case you're a beginner like me, buy a few extra tips to ensure smooth learning and timeline development for your projects.

In the case that your tip oxidizes, be sure to set the heating temperature within recommended conditions, and to clean it using tip tinner cleaner and copper coated sponge. 

<img width="1000" height="1250" alt="IMG_3746" src="https://github.com/user-attachments/assets/eb95ca61-e6ea-493a-bc4f-958bc96b4e91" />
<img width="1250" height="1000" alt="IMG_3745" src="https://github.com/user-attachments/assets/f62d983c-8c03-427a-8b92-ace94ba4ff6b" /> </br>
After soldering it may look like this. Note that due to the rosin being used, it must require clean up as it is hardened. Unfortunately one of the four pins is heavily scratched due to accidental large amounts of solder originally sticking to 3 of the pins. I had to manually scrap it to get it off as the solder wasn't melting regardless of using flux, different temperatures and other tools.

Here, we now need to repair the traces, and we also need to re-add the solder mask, and do continuity tests with a multi meter to check for signal integrity. As such, copper wires are needed. The repair itself is fairly straightforward, using the existing solder nodes and linking the ripped traces with copper wires, it can be repaired and look as such. Also, testing with the multimeter after to confirm that there is no obscure values for resistance, it is shown to be around 2 to 3 ohms for each node.

<img width="1250" height="1000" alt="IMG_3955" src="https://github.com/user-attachments/assets/32ba14ab-9305-4afe-a879-896234c2da98" />
<img width="1250" height="1000" alt="IMG_3956" src="https://github.com/user-attachments/assets/73014c33-1406-4816-8a47-d330b5cd605e" />

Note to self, definitely stick the breadboard onto the pcb first before soldering the female pin heads to the pcb. Otherwise it's very easy to have it misalign (also not really possible to unstick the breadboard once its touching the pcb).
<img width="1000" height="1250" alt="IMG_3763" src="https://github.com/user-attachments/assets/bfbc8c44-55dd-4690-a36f-aaf0e8b0f1b9" />

After getting everything soldered on and placed properly, the first circuit to test will be a low pass filter (LPF).
<img width="904" height="388" alt="Screenshot 2026-08-31 213839" src="https://github.com/user-attachments/assets/7838fe73-c6c7-46c4-95be-e94860fa54d2" />
How this works can be interpreted using KCL. It can be seen as below.
<img width="4030" height="1354" alt="IMG_4163" src="https://github.com/user-attachments/assets/487126c8-afc8-4216-9ef8-df28e0e58357" />
<img width="4030" height="1977" alt="IMG_4164" src="https://github.com/user-attachments/assets/3ac33ba0-597f-4f9e-ae2f-24d27402247a" />
Note that for the capacitor calculation segment, we are using Laplace's transform to convert from time to frequency. Recall that Laplace transform (time -> frequency) integrates a function across time, and for inverse Laplace transform (frequency -> time) integrates a function across frequency.

As for a high pass filter (HPF), simply swapping the resistor and capacitor should do it. Likewise, using KCL can obtain the equations needed as such.
<img width="1647" height="3148" alt="IMG_4170" src="https://github.com/user-attachments/assets/5dbc8f36-128d-4849-b3cc-c8e16e987e37" /> <br/>
The actual circuit would look like this on the breadboard.
<img width="1823" height="3478" alt="IMG_4172" src="https://github.com/user-attachments/assets/2335d569-ef11-40a6-b80a-33fd8943b8d6" />



If we want to cut off more frequencies for the LPF, we may need to consider a cascading circuit.







