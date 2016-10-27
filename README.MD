This document outlines the XFR Collective’s digitization workflows. You will find in this document how to operate the rack and specific machines to achieve a successful transfer as well as administrative workflows that will keep the quality of our files and metadata. We have described every step of the process, starting with general knowledge you must have before operating the system. We have done our best to include as much information as possible about troubleshooting and problems we’ve had with certain pieces in the chain.

[[TOC]]

# 1.	XFR Rack Components

This section reviews the components of the rack, except for the playback decks, which are described by format in the transfer workflows. 

## 1.1.	Monitors

### 1.1.1.	CRT Monitor (Pre and Post)

(Model: JVC-H150CG)

Using the Sony video monitor we are able to monitor the image before digitization (Pre) and after (Post).  We have labeled both in the front (photo below). Make sure you connect a secondary video output from the deck to the Video A input of the monitor and a video output from the AJA to the Video B input (either BNC or S-Video would work). 

![Image of Model JVC-H150CG](WorkflowDocumentation/images/JVC-H150CG-01.png)

Left: Pre and Post switches in the front of the Sony monitor. Right: Video inputs of the Sony monitor. Note that you can use only BNC for input A, and BNC or S-video for input B. Just make sure you use only one type of input for Video B, we had some issues with the monitor when connecting both at the same time.

### 1.1.2.	Audio Monitor (Post only?)

(Model: Wohler Technologies AMP 1A Analog Audio Monitor Panel)

![image alt text](image_2.jpg)

*Front of the audio monitor.*

On the front of the audio monitor, there are knobs for volume and balance. Note that the audio monitor does not have a power switch -- it just turns on when the rack when it is plugged in.

### ![image alt text](image_3.jpg)

*Back of audio monitor.*

The audio monitor has one set of balanced right and left XLR inputs, which we have set up to monitoring post-digitization audio, but it can be switched to pre-digitization monitoring if needed. Besides the balanced XLR inputs, there are unbalanced inputs, which we are not using. There is also a XLR loop-through, but we’re not sure how it can come in handy in a workflow.

![image alt text](image_4.jpg)

*XLR outs on the back of the AJA.*

The audio monitor receives the post-digitization audio signal as analog audio from XLR outs on the AJA. 

### 1.1.3.	Waveform Monitor (Post only)

(Model: Tektronix WFM 601E Serial Component Monitor)

![image alt text](image_5.jpg)

The Tektronix WFM 601E Serial Component Monitor is BOTH a waveform monitor AND vectorscope.  To switch from waveform monitor to vectorscope, press the Vector or Waveform buttons on the Display Menu in the front.

 

![image alt text](image_6.png)

*Display Menu of the Tektronix Monitor*

The waveform monitor allows us to monitor the video signal. Wikipedia says: "It is typically used to measure and display the level, or voltage, of a video signal with respect to time." This monitors allows us to control the overall levels of the video signal, making sure it doesn’t go over standard limits. When using the SMPTE Color Bars, the white can’t go over 100 IRE and the black must be at 7.5 IRE (dotted line on monitor screen).

To adjust the levels we use the Time Base Corrector (TBC) explained below.

 

 ![image alt text](image_7.png)

 

Waveform monitor showing SMPTE Bars correctly adjusted.

  

### 1.1.4.	Vectorscope (Post only)

(Model: Tektronix WFM 601E Serial Component Monitor)

The Tektronix WFM 601E Serial Component Monitor is BOTH a waveform monitor AND vectorscope. To switch from waveform monitor to vectorscope, press the Vector or Waveform buttons on the Display Menu in the front.

 

![image alt text](image_8.png)

*Display Menu of the Tektronix Monitor*

The vectorscope is another way of monitoring video signal. In this case, we can see the color information. The monitor shows information about red, green, blue, yellow, magenta and cyan. We can adjust those values using the TBC. When using the SMPTE Color Bars, the monitor shows all dots matching the squares of each color.

![image alt text](image_9.png)

** **

Vectorscope showing SMPTE Bars correctly adjusted.

** **

### 1.1.5.	RF Monitor (U-matic only)

**(**Model: Tektronix Type 528 Waveform Monitor (even though we use it as RF))

We use the RF monitor to transfer U-matic tapes because it is the only deck that has an RF output. It is useful for seeing if the heads are misaligned, which is a common problem with U-matics. This step allows obtaining the highest level of signal from the tape, by aligning the heads with the video tracks. Erik Piil wrote a blog post about this, which is available in PDF in our Google Drive: [https://drive.google.com/drive/u/2/folders/0B9yFlIIX5_YicHRzcTlpX04zZUk](https://drive.google.com/drive/u/2/folders/0B9yFlIIX5_YicHRzcTlpX04zZUk)

 

![image alt text](image_10.png)

 Front of the RF monitor.

 

To use this scope, simply connect the RF output of the U-matic deck to the Video A input of the scope. Then, connect the monitor video output to the external reference of the scope. This last step is fundamental, since the scope needs the video signal as a reference to operate correctly. This also means that we will not connect the sync generator to the RF monitor.

 

Then, adjust the skew switch in the front of the U-matic deck, to obtain the highest waveform on the scope. This switch allows to control tracking.

![image alt text](image_11.png)

Skew switch in front of U-matic deck.

 

Since we are using the only Monitor Video Out the U-matic deck has, we need to take advantage of the loop through, mentioned in section 1.1. to have PRE video monitoring for U-matic. To do so, connect the looped output of the EXT REF input on the RF Monitor (instead of using a terminator) to the Video A input of the CRT monitor.

** **

** **![image alt text](image_12.png)

** **

Back of RF Monitor showing EXT SYNC loop (bottom BNC cable)

connected to the video monitor (input video A)

** **

## 1.2.	Cables

** **

There are several types of cables used in the rack. Since we yet don’t have a switcher or patch bay, we normally have to re-route connections in the back of the rack every time we want to transfer a tape. For this reason, it is a must to know all types of cables, to know which one to use. 

** **

* **BNC:** This is used normally for the composite video connection. This cable transports all three YUV signals in one cable.

* **S-Video:** This cable separates luminance and chrominance (UV combined). It is still composite video, but since both signals are separate, it prevents interference.

* **RCA:** Also a composite type of cable, widely used in the consumer market.

* **XLR** Male and Female: XLRs are professional cables, used primarily for audio. There are male and female versions, in both cables and machine connectors. If you want to use this cable, make sure you have the right type.

* **FireWire** all types: FireWire is a digital interface, with different connectors (4, 6, 9 pins) and different protocols of data transmission (400, 600, 800).

* Note on **SDI** Connections: all SDI (Serial Digital Interface) connections in the rack are BNC.

![image alt text](image_13.png)

![image alt text](image_14.png)

Good websites if you want to know more about cables:[ http://www.infocellar.com/television/component-svideo-composite.htm](http://www.infocellar.com/television/component-svideo-composite.htm)

[https://github.com/amiaopensource/cable-bible](https://github.com/amiaopensource/cable-bible)

**Note:** Please use cable ties (blue Velcro things) when cables are not in use. It helps keep things organized and easy to find.

## 1.3.	Terminators

Some video connections have a linked connection known as the "loop though" marked with a line, as shown in the picture below. This means that, whatever signal is plugged to the first connector will be copied to the other. By using a terminator (connected to the second A output in the photo) we avoid having interference in the signal. Some machines have a 75 Ohms switch incorporated. To activate the termination put the switch in ON.

 

There’s a good explanation of this here: My Drive > XFR_C_Documentation > Useful Docs and Manuals  > Video_setup_Basics.pdf

![image alt text](image_15.png)

Back of RF monitor showing the linked output terminated.

## 1.4.	(External) Time Base Corrector (TBC)

(Model: Digital Processing Systems DPS-290 Component TBC / Synchronizer)

Wikipedia says: "Time base correction is a technique to reduce or eliminate errors caused by mechanical instability present in analog recordings on mechanical media. Without time base correction, a signal from a videotape recorder (VTR) or videocassette recorder (VCR) cannot be mixed with other, more time stable devices found in television studios and post-production facilities. Most broadcast quality VCRs have simple time base correctors built in though external time base correctors (TBCs) are often used."

In our case, we use the external TBC for U-matic, Betacam and consumer VHS. The Professional VHS deck has a quite good and robust built-in TBC.

 

The external TBC has two sections that we use often:

* Under "Select," the Input button: NTSC for BNC In and SVID for S-Video In.

* Under "Proc Amps," these buttons and the wheel will help us adjust luminance and chrominance.

* **Video**: controls luminance amplitude (White level: ideally 100 IRE)

* **Black**: controls black level (second stair on the waveform monitor, ideally 7.5 IRE, right on the dotted line).

* **Chroma**: controls amplitude of the chrominance (color intensity, how big is the radius of the circle on the vectorscope monitor).

* **Hue:** controls color phase (by adjusting this parameter you can turn the color circle on the vectorscope).

 

![image alt text](image_16.png)

*Front of the DPS-290 TBC.*

 

 

##  1.5.	Analog-Digital Converter (AJA)

(Model: AJA IO 101351)

![image alt text](image_17.png)

##  1.6.	Sync Generator

(Model: Horita BSG-50 Blackburst Sync Gen)

The black-burst sync generator Horita BSG-50 is a little black box. It gives out a continuous "blank" pure video signal. Ideally, all equipment would be connected to the sync generator through its “sync in” or “reference/ref” input. This will allow the whole system to work smoothly, keeping all equipment “communicated” with each other.  If the system is out of sync, you may get errors in your transfer.

 

Unfortunately not all equipment has a sync connection. Our CRT monitor, for example, does not have one (otherwise it would ideally be connected too). Also, don’t connect the RF monitor to the sync generator, since this input will be used for other purposes (See Sections: RF Monitor and U-matic).

![image alt text](image_18.png)

 

Make sure you connect to the "sync in" and not the “sync out”, this means that the device is receiving a sync signal as a “slave”, following the generator as a reference.

 

The Horita generator has 6 black-burst outputs (BLK) – they’re all the same. All outputs are BNC connectors. There’s also a 1kHz reference audio output, but we are currently not using it.

 

Important note: this device has a special power connector (1/8" or 3.5 mm plug, Output is 9VDC, 500 mA, positive tip). If it breaks we have to order it directly from Horita or special seller. It’s not expensive, but we don’t want to go through that again.

 

![image alt text](image_19.png)

Horita Sync Generator, 6 black burst outputs, one 1kHz audio output.

 

** **

# 2.	Receiving and Preparing Tapes from Partners

This section outlines the steps for handling partner tapes to ensure understanding with partners, control over tapes in our care, and a smooth workflow.

## 2.1.	Partner Agreement and source metadata

A signed partnership agreement should be in place before tapes are exchanged and transfers begin. Partner Agreement template:

[https://docs.google.com/document/d/11fZOE4jqp3nOl6uHIk7LHxnUb63rQe4fo47bS0SSJ2k/edit](https://docs.google.com/document/d/11fZOE4jqp3nOl6uHIk7LHxnUb63rQe4fo47bS0SSJ2k/edit)

The partner should also fill out the metadata questionnaire (Appendix A in the Partnership Agreement). This information is essential for knowing whether the content can be uploaded on Internet Archive, how it should be described and attributed, and how it should be CC-licensed.

Some partners ask for an invoice for their partnership fee. The invoice template:

[https://drive.google.com/open?id=0B9yFlIIX5_Yicnd5SjVlRGVEVDg](https://drive.google.com/open?id=0B9yFlIIX5_Yicnd5SjVlRGVEVDg)

## 2.2.	Create tape manifest with partner

When we receive the tapes from a partner, itemize the tapes on a Receipt Form with the partner: [https://docs.google.com/document/d/1jalI4_9nZHLJe5Ft4KdNv2poqQGtcqBToM7bzoEOg7g/edit ](https://docs.google.com/document/d/1jalI4_9nZHLJe5Ft4KdNv2poqQGtcqBToM7bzoEOg7g/edit)

## 2.3.	Store and label tapes

Keep materials from one organization in one bag/box so they don’t get lost or confused with other stuff. Label the bag and put the number and format of tapes in it.

 

Put a XFR sticker on the tape and write down the date it was received. We then assign a unique ID for every tape, following this convention:

 

        	*        	Member_00X*

 

If the member already has a numbering system, you can use their numbering system. This ID will be used for the Reel number in FCP, which will become the filename. 

## 2.4.	Create a metadata spreadsheet for each partner 

For each partner, create a metadata spreadsheet in the Partners folder using this template:

[https://docs.google.com/spreadsheets/d/1yuobKNXIv2b6adGnnnI2_X1fpELyZomO95ghqp06kz0/edit#gid=5](https://docs.google.com/spreadsheets/d/1yuobKNXIv2b6adGnnnI2_X1fpELyZomO95ghqp06kz0/edit#gid=5)

You can enter basic metadata, such as unique ID and tape format for each item prior to transfer. The rest of the metadata will be entered after the transfer (see further in this manual). 

# 3.	Set-Up for All Transfers** **

In this section you’ll find the basic preparation steps to start transferring. Some of them seem very obvious, but I wanted to be as thorough as possible, leaving minor space for errors. It’s always good to use this as a checklist; there are so many details that you can easily forget some of them.

## 3.1.	Plug in and turn on

We normally keep the rack unplugged, so don’t freak out if nothing turns on! There’s a plug strip stuck to the side in the back of the rack where all machines are plugged. Plug the strip to the extension, using the big round plug:

 

 ![image alt text](image_20.png)

Most of the On switches are on the front of the decks. The On switch for the AJA is at the back. Remember to turn on the sync generator too.

 

## 3.2.	Clean deck heads

** **

Before every transfer, make sure to clean the deck heads. The heads are on the drum inside the machine. To do so, first make sure the deck is off. Then open the top cover. Take a lint free cloth and some isopropyl alcohol and place the cloth on the side of the drum, pressing lightly on the head. With the other hand, slowly turn the drum. Repeat until the cloth comes out clean. Be careful while doing this, heads are precious!

 

You should also clean the tape guides (the metal things that take the tape out of the cassette and put it around the drum) and audio heads.

 

Important: don’t clean the pinch roller. The plastic will absorb the alcohol, which causes the roller to dry out.

 

You can see a video of us cleaning the consumer VHS deck on our Google Drive: My Drive/XFR_C_Audios&Videos/July6th2015_Training.

 

![image alt text](image_21.png)

*Cleaning our consumer VHS deck.*

** **

## 3.3.	Set TBC values to zero (and select correct input on the front panel).

** **

Ideally, we would want to calibrate the TBC first, using SMPTE bars, but right now we don’t have that capability. Therefore, we set all values of the TBC to zero: on the front panel, in the "Proc Amps" section, select *Video *and turn the knob until the screen shows “000”. Repeat the process with *Black*, *Chroma*, *Balance* and *Hue*.

 

You have to also make sure that you have selected the correct input on the "Select" section (NTSC for BNC and SVID for S-Video).

 

## 3.4.	Check connections for format you want to digitize

** **

Because we don’t have a switcher or a patchbay, every time we want to digitize a specific video format we need to check or manually change the connections in the back of the rack. Each format has its own particular signal chain. See the workflow diagrams in this document below. 

Component is the best option. S-video is the second best. Composite is the third best. If your deck has more than one, use the highest quality output available (you can use the secondary ones for monitoring).

Most U-matic decks, including ours, output a composite signal. You could also output from "Dub," which is a Y/C out (like S-video), but we don’t have the cable. 

 

Our VHS outputs a S-video (luminance and chrominance channels) signal. There is also a composite out.

Betacam uses a component (aka YPbPr) signal.

* Y = green + lum + sync

* Pb = lum - red

* Pr = lum - blue

**Once all connections are checked, you can turn on all equipment, including the computer.**

** **

## 3.5.	 Connect AJA & Open AJA VTR Xchange software

Before running the software, first thing is to check that the AJA is connected to the computer via Firewire.

![image alt text](image_22.png)

AJA Driver connected to the tower via FireWire.

Then, open the AJA Driver (on dock). This helps us check that the rack and computer are communicating correctly. 

 ![image alt text](image_23.png)

Icon for AJA software

Put a test tape in the deck. Go to Capture > Video Settings…  and see if you get an image on the small screen. If not, check the connections. If the problem persists you probably want to turn off and on the whole rack to allow the system to reset. 

![image alt text](image_24.png)![image alt text](image_25.png)

NOTE: sometimes the AJA Driver doesn’t work correctly when reproducing video. We don’t know why, but every time we check and uncheck the "preview" box it seems to respond. Oh, we love machines!

**Make sure you close the driver before opening Final Cut, sometimes they’re not very good friends! **As a general note, try not to open more programs than needed on the computer. This is just to keep the transfer as smooth as possible.

## 3.6.	Deck Calibration

Ideally, we would use a test tape to calibrate the deck. This is basically to "re-set" the deck, in case it was adjusted a lot previously.  You should still calibrate to the specific tape you’re capturing.

## 3.7.	CRT Monitor Calibration

** **

We can calibrate the CRT monitor using the AJA VTR Xchange and the blue screen on the monitor. To do so, open the SMPTE Color bars video (on the Desktop) in AJA VTR Xchange. Make sure you are looking at the POST signal on the CRT.

 

Adjustments are made using the chroma/phase button on the front:

 

 ![image alt text](image_26.png)

 Press once to adjust chroma, twice to adjust phase.

 

![image alt text](image_27.png)![image alt text](image_28.png)

To calibrate, first turn the chroma all the way down so that the image is black and white. Look at the three thin black lines in the lower right side of the SMPTE bars (representing 3.5, 7.5, 11.5 IRE, respectively). Adjust the brightness so that:

* The leftmost and middle bars are the same as the larger black square next to them.

* The rightmost bar is barely brighter than the other two bars.

Turn the contrast all the way up, so that the rightmost black bar is bright. Adjust the contrast back down until you can barely see that black bar.

![image alt text](image_29.png)

Now, select the "Blue Check" button on the CRT monitor and make sure you are looking at the POST signal. The color bars should appear in blue.  

* Adjust the chroma so that the tops and bottoms of the long blue stripes match.

* Adjust the chroma so that the outer (far left and far right) blue bars match.

* Adjust the phase so that the middle two blue bars match.

 

![image alt text](image_30.png)

## 3.8.	Create folder for each member

** **

We currently have two internal hard drives in the computer: *3 TB One* and *3 TB Two*, and we normally use the one that has the most space available.

 

Create a folder following the naming convention: *XFR_Collective_MEMBER_Year*

 

This folder will contain all digitized videos and metadata for that particular project. If there are more batches from the same member, we add a number at the end: *XFR_Collective_MEMBER_Year_2*. We also keep separated metadata for each batch, since the membership model works for batches of 6 tapes.

## 3.9.	Open Final Cut and select correct settings

Open/Create a Final Cut project.

Go to Final Cut Pro > System Settings.

 ![image alt text](image_31.png)

 

On the Scratch Disks tab, click on Set in the first row and select the member folder you previously created. Note that this will create a new folder in the member folder called Capture Scratch and Final Cut will do this every time you change the settings. It’s all right, as long as all the video files end up in the member folder. You can always get rid of these annoying folders and reconnect media if necessary.

 ![image alt text](image_32.png)

 

 Then, go to Final Cut Pro > Audio/Video Settings.

 

 ![image alt text](image_33.png)

### 3.9.1.	FCP Settings for transferring analog media

 ![image alt text](image_34.png)

### 3.9.2.	FCP Settings for transferring MiniDV

![image alt text](image_35.png) 

### 3.9.3.	FCP Log and Capture

Open the Log and Capture screen (Command+8). In the Logging tab, make sure to change the Reel and Description. Use the final desired file name: *MEMBER_00X*. If there’s more than one batch from a member, we continue with the next number, so we don’t create duplicate file names.

 

If you stop and re-start a capture, note that **FCP will automatically change the reel number to the next sequential number.** Check and correct as needed, or else your filenames will not match the tapes. 

 

![image alt text](image_36.png)

On the Clip Settings, make sure the Video and Audio checkboxes are checked and that both audio channels are on (green) and linked (button on the left). If you’re transferring analog media, you will see four tracks. You must turn on only the first two.

![image alt text](image_37.png) 

 

On the Capture Setting, make sure the options are the same you selected in the Audio/Video Settings.

** **

** **

** **

## 3.10.	Check for audio** **

Now you need to check that Final Cut is receiving video and audio. Playback a section of the tape to check. Audio levels (if there are any) should show on the meters at the bottom right of the screen. If you’re not getting any audio you can check if there’s audio on the tape by using the audio monitor or connecting headphones directly to the playback deck.

 

![image alt text](image_38.png)

If the deck has an output level control you can use these meters to adjust levels.

 

Note: **there is no real time audio monitoring in Final Cut during transfer**, so checking for audio before is very important.

 

## 3.11.	Calibrate video

 

We calibrate the video using the TBC. If the tape has bars at the beginning, we adjust the levels using the TBC and scopes.

 

If there are no bars, we at least want to make sure that the white doesn’t go above 100 IRE. 

![image alt text](image_39.png)

If you can find any skin tone you can calibrate using the vectorscope. You can also check colors by comparing the PRE and POST image.

![image alt text](image_40.png)

 

Now you’re ready to start capturing! Rewind the tape. Click the Now button below and Play on the deck.

** **

# 4.	Workflows and Wiring By Format

## 4.1.	VHS/ S-VHS / VHS-C

(Pro S-VHS Model: Sony SVO 5800 Video Cassette Recorder)

(Consumer VHS Model: Sharp VC-H960)

(Consumer S-VHS Model: Panasonic AG-3200)

We currently have two VHS decks: a professional one and a consumer one. Although the professional one has a better quality, it doesn’t play EP (Extended Play) mode tapes (tapes that run at a slower speed). In addition to that, some VHS tapes have hi-fi audio recorded in a different track that normally can’t be played back using the professional deck (if the tape seems to have audio but the deck won’t play it back, this is probably the case).

 

Try using the professional one first (in the rack), and if it doesn’t play, switch to the consumer one.

 

We have a VHS-C adapter, which can be used in both decks. To put the tape in the adapter, slide the lid open and insert the tape. When you close the lid the adapter’s mechanism will lift the tape’s lid and expose the tape. Then the tape is ready to insert in the deck.

 

![image alt text](image_41.png)

*VHS-C Adapter*

** **

Note: If you use the Professional deck, there’s no need to use the external TBC, since the internal TBC is good enough and will compensate better for errors.

Our VHS outputs a S-video (luminance and chrominance channels) signal. There is also a composite out.

### 4.1.1.	 Professional VHS Deck Video Wiring Diagram

 ![image alt text](image_42.png)

### 4.1.2.	Professional VHS Deck Audio Wiring Diagram![image alt text](image_43.png)

Note: Do not connect to AJA AES/EBU inputs.

### 4.1.3.	 New VHS Pro Deck Video/Audio Wiring Diagram (with Audio monitor)

![image alt text](image_44.jpg) 

### 4.1.4.	Consumer VHS Deck Video Wiring Diagram

![image alt text](image_45.png)

### 4.1.5.	Consumer VHS Deck Audio Wiring Diagram![image alt text](image_46.png)

 Note 1: Do not connect to AJA AES/EBU inputs.

Note 2: To connect these you must use the RCA-Male XLR cables. Ideally we would want a direct box to convert from RCA to XLR (to regulate impedance) but we don’t have it yet.

Note 3: the TBC and the AG-3200/consumer VHS  deck do not always play nicely together; when using the AG-3200 VHS consumer deck, extensive TBC alterations can cause time-base correction errors in the digitized file.

## 4.2.	U-matic / Umatic SP

Model: Sony VO-9850

** **

We only have one U-matic deck that will play back both small and large U-matic tapes.  

Most U-matic decks, including ours, output a composite signal. You could also output from "Dub," which is a Y/C out (like S-video), but we don’t have the cable. 

 

To digitize U-matic tapes we will also use the RF monitor, to adjust tracking (i.e., alignment between the heads and the recorded signal) for maximum signal output.

### 4.2.1.	U-Matic Video Wiring Diagram

** **![image alt text](image_47.png)

### 4.2.2.	U-Matic Audio Wiring Diagram

![image alt text](image_48.png)

Note 1: Do not connect to AJA AES/EBU inputs.

** **

## 4.3.	Betacam/ Betacam SP

Model: BTS BVW-75

We have one Betacam deck that plays back Betacam and Betacam SP and both small and large cassettes.

Betacam uses a component (aka YPbPr) signal.

* Y = green + lum + sync

* Pb = lum - red

* Pr = lum - blue

### 4.3.1.	Betacam Video Wiring Diagram

### ![image alt text](image_49.png)

### 4.3.2.	Betacam Audio Wiring Diagram

![image alt text](image_50.png)

Note 1: Do not connect to AJA AES/EBU inputs.

 

## 4.3.	Video 8 / Hi-8 / Digital 8

Model: Sony GV-D200

The Video 8 / Hi-8 / Digital 8 deck is the tiny deck that sits on the shelf on the rack.

![image alt text](image_51.jpg)

### 4.3.1 Menu Settings

Press Menu button on deck to display menu on CRT monitor. Use these settings:

Hi Fi Sound: STEREO

PB Mode: AUTO (unless deck doesn’t recognize video, then try Hi8/8)

Turn A/V → DV Out: OFF

TBC: OFF  (we are using external TBC)

DNR: ON? 

![image alt text](image_52.jpg)

## 4.4.	MiniDV

Model: Sony [need model #]

MiniDVs are transferred directly to the computer without the use of the AJA or any other equipment in the rack, since MiniDVs store digital video. To do so we connect the MiniDV deck to the computer using a FireWire cable.

** **

![image alt text](image_53.png)

MiniDV Deck connected to the computer using the FireWire cable.

** **

You can also have a pre monitoring setup by connecting the video and audio outputs to the video monitor using RCA cables. You can either use the monitor in the rack or the other one (for this one you need a BNC-RCA adapter for the video connection).** **

 

 ![image alt text](image_54.png)![image alt text](image_55.png)

Left: MiniDV deck analog outputs. Right: Inputs for the second video monitor, note that if you use this one you can only connect one audio channel.

## 4.5 	Audio cassettes

Model: Akai HX-A301W

For audio transfers we will use the AJA and Final Cut. Final Cut it’s not the best software for audio, but the AJA doesn’t work if it doesn’t get some video signal.

  

To transfer audio, open a regular Final Cut project. All settings are the same, except that this time we need to UNCHECK the video box on the Clip Settings tab on the Capture Screen. Make sure audio channels 1 and 2 are on and linked (chain symbol on the left side of the meters). Channels 3 and 4 must be off.

 ![image alt text](image_56.png)

Final Cut settings for audio transfers. Video box is unchecked.

 

### 4.5.1.	Audio Cassette Wiring Diagram

![image alt text](image_57.png)

 Note: There’s no need to use the TBC for this purpose, any video signal will suffice. I normally use the VHS because tapes are longer, so I don’t "run out" of video while transferring audio. So you can use any tape. I am currently using a very nice long tape titled “If Tomorrow Comes”. This 90’s soap opera is so much fun :P

 

Please use headphones when digitizing audio, since there’s no image reference to know when the tape is over.

 

### 4.5.2.	Exporting Audio Files

While transferring you will still see the video, but Final Cut will only be capturing audio. Unfortunately, the resulting files are .mov wrapped. Remember that I mentioned Final Cut doesn’t like audio very much?  Anyway, this is fine, but we prefer .aiff or .wav files.

 

To re-wrap the file:

 

* Drag the audio file from the Browser window to the timeline.

* Select the audio file (it looks dark when it’s selected):

 ![image alt text](image_58.png)

* Go to File > Export > Audio to AIFF(s):

 ![image alt text](image_59.png)

* Select the destination folder, Rate (48kHz), Depth (24-bit), Config (Stereo Mix):

![image alt text](image_60.png)

Note: Don’t use Media Streamclip for this process because it doesn’t allow bit depths higher than 16 bits.

 

## 4.6.	DAT 

** **

# 5.0.	Post-Transfer Workflows

## 5.1.	Completing the capture

To end a transfer just press ESC. Then, close Final Cut and go to the Capture Scratch folder where the video was stored. Check the file name. If it doesn’t match to the tape’s label, change it (keep in mind that if you change it, the next time you open Final Cut it won’t find the file and you’ll have to Reconnect Media if you need it).

 

Open the video and perform a spot check to make sure the audio and video are ok.

Also check that the filename is correct (FCP auto re-names files when you re-capture tapes).

## 5.2.	Run checksums

Because the creation of checksums can take a long time for big video files, you might want to do this after you’ve finished transferring for the day. However, make sure you do it as soon as possible, so you don’t forget!

 

The simplest way of creating a checksum for a single video file is:

 

* Open Terminal

* Type *md5, *space, and* *drag the video file to the terminal window and hit enter.

* Copy the 32-character checksum to the metadata spreadsheet.

** **

However, this would only allow to create checksums for one file at a time. If you want to save time and let the process run overnight, you can follow the step below. 

 

**Method 1**

In Terminal:

* Change location to the folder where the videos are located using the cd command:

$ cd [directory]

Note: the command *cd .. *will take you one level above. The command *ls *will list all files in the folder you are currently in. Terminal doesn’t like folders that have spaces in their names. If you want to type a folder path for a folder that has a space you have to replace every space with "\ “ (including the space).

 

* Type the following:

 

$ find . -type f -exec md5 '{}' \; >> [something].csv

 

Replace [something] with the filename you want to assign. This command will find all files in the current folder, execute an md5 checksum for each and save all checksums in a csv file (which you can open using excel.

**Method 2**

Download and install md5deep: [http://md5deep.sourceforge.net/](http://md5deep.sourceforge.net/)

In Terminal, type:

$ md5deep -rte the/directory/the/files/are/in > mydirectory/md5.txt

The "-r" means “recursive” so that it will look for all the files inside the directory. 

The "-t" means “timestamp” so the date and time that the checksum was run will be printed with each result.

The "-e" means “time remaining” so you can how much time is left to process the checksum.

## 5.3.	Complete the metadata form

Finish filling in the Google spreadsheet with basic metadata for each tape transferred. Include any problems or observations in the Notes field.

## 5.4. 	Quality assurance checklist / diagnostics

<table>
  <tr>
    <td>✅</td>
    <td>Quality</td>
    <td>Method</td>
  </tr>
  <tr>
    <td></td>
    <td>File opens and plays.</td>
    <td>Open and play the file.</td>
  </tr>
  <tr>
    <td></td>
    <td>File is valid and well-formed. </td>
    <td>(How should we do this?)</td>
  </tr>
  <tr>
    <td></td>
    <td>Capture is complete. </td>
    <td>Check end of file and overall duration.</td>
  </tr>
  <tr>
    <td></td>
    <td>Format, frame rate, channels of audio, and aspect ratio is correct.</td>
    <td>Visually inspect and check technical metadata using MediaInfo.</td>
  </tr>
  <tr>
    <td></td>
    <td>Audio is present, at correct level, and synced to video.</td>
    <td>Watch and listen to samples from beginning, middle, and end of file.</td>
  </tr>
  <tr>
    <td></td>
    <td>Errors due to TBC, mechanics, and tape damage have been addressed to best of our ability.</td>
    <td>See Issues and Diagnosis chart below.</td>
  </tr>
  <tr>
    <td></td>
    <td>Filename is correct.</td>
    <td>Check filename against tape label and file naming rules.</td>
  </tr>
  <tr>
    <td></td>
    <td>Storage location is correct.</td>
    <td>Check that file is in correct partner folder.</td>
  </tr>
  <tr>
    <td></td>
    <td>Checksum is generated.</td>
    <td>Check that MD5 is recorded in spreadsheet.</td>
  </tr>
  <tr>
    <td></td>
    <td>Preservation metadata is recorded.</td>
    <td>Check that preservation metadata is recorded.</td>
  </tr>
</table>


<table>
  <tr>
    <td>Issue</td>
    <td>Diagnosis</td>
  </tr>
  <tr>
    <td>TBC Errors</td>
    <td></td>
  </tr>
  <tr>
    <td>Areas like sky are too white / bright.</td>
    <td>High Video Level</td>
  </tr>
  <tr>
    <td>Colors look pale or washed out.</td>
    <td>Undersaturation</td>
  </tr>
  <tr>
    <td>Colors are too intense and bleeding.</td>
    <td>Oversaturation</td>
  </tr>
  <tr>
    <td>Fuzzy specks of color in dark/black areas.</td>
    <td>Chrominance Noise</td>
  </tr>
  <tr>
    <td>Brightness noise, like translucent snow over picture.</td>
    <td>Luminance Noise</td>
  </tr>
  <tr>
    <td>Wrong colors.</td>
    <td>Hue</td>
  </tr>
  <tr>
    <td>Luma/chroma not aligned. Blurred edges between areas of high contrast.</td>
    <td>Y/C Delay Error</td>
  </tr>
  <tr>
    <td>Skewy lines or shaky picture.</td>
    <td>TBC Processing Artifact</td>
  </tr>
  <tr>
    <td>Mechanical errors</td>
    <td></td>
  </tr>
  <tr>
    <td>Lines and distortion in picture</td>
    <td>Tracking Error</td>
  </tr>
  <tr>
    <td>Stretched skewy lines at top or bottom of picture.</td>
    <td>Skew Error</td>
  </tr>
  <tr>
    <td>Parts of image obscured or missing.</td>
    <td>Video Head Clog</td>
  </tr>
  <tr>
    <td>Horizontal line at bottom of picture.</td>
    <td>Head Switching Noise</td>
  </tr>
  <tr>
    <td>Rainbow line at top or bottom of picture.</td>
    <td>Timecode Error</td>
  </tr>
  <tr>
    <td>Tape Damage</td>
    <td></td>
  </tr>
  <tr>
    <td>Missing line or spot / snow</td>
    <td>Dropout</td>
  </tr>
  <tr>
    <td>Horizontal rolling line.</td>
    <td>Tape Crease</td>
  </tr>
</table>


# 6. Access

## 6.1.	Clean up Partner folder

Once all the transfers for the Partner are complete, clean up the Partner folder.

* Move all the completed transfers from the Capture Scratch folder to the top level of the Partner folder.

* Delete the FCP render, auto-save, and cache files, which are unnecessary.

## 6.2.	Transfer files to Internet Archive

There are two ways that we transfer preservation masters to Internet Archive: hand-delivery of a hard drive, and web upload.

### 6.2.1.	Transfer to Internet Archive via hard drive / hand delivery

For hand delivery, Andrea typically brings the hard drives to Internet Archive when she travels to California. Our contact there is Jeff Kaplan <[kaplan@archive.org](mailto:kaplan@archive.org)>.

To transfer files to a hard drive for delivery, you can use the conventional drag and drop method, although for a large copy job it is better to use a tool that will allow you to restart interrupted transfers and check that your job completed. Rsync is a good tool for this.

Type:

$ rsync –vaP directory/to/be/transferred destination/on/hard/drive

* *

Example:

$ rsync –vaP Volumes/3TBTwo/XFR_Collective_NYWIFT Volumes/XFR_Drive1

* *

The "-v" means that Terminal will print a verbose output of what it’s doing.

The "-a" means “archive” which means that it will look recursively in the directory and preserve most of the file attributes.

The "-P" means “Progress” which means Terminal will tell you it’s percentage progress.

This command will preserve all metadata and permission settings, It also shows the transfer progress.

 

Rsync has a way to validate the files it transfers to ensure file integrity, but if you want to be extra sure, you can run checksums on the copied files and see if they match your previously calculated checksums.

### 6.2.2.	Transfer to Internet Archive via web upload

An alternative to hand-delivering hard drives is to upload files one-by-one over the web. For large files, this can several hours or even a day to upload a file. 

## 6.3.	Add metadata to Internet Archive records

**9** 	** Delivering Files and Tapes to Members**

** **

Some members ask us for a copy of the video files. There are certain considerations for this:

 

-       Make sure to ask for a big enough hard drive: Although we can, we normally don’t create access files, we just don’t have enough time and members can ultimately download these from the Internet Archive or generate their own.

-       Copy in the drive the metadata spreadsheet.

 

When returning tapes, normally after we’ve checked that the files are on the Internet Archive, we also fill out a Release Form. You can find the template in My Drive > XFR_C_Documentation > Receipt_Release_Forms. Make sure both parties sign.

 

In that folder there’s also a Cover Sheet, where we describe the contents of the hard drive delivered. Please add that to the packet.

 

 

**1.**  	**Creating Derivatives**

** **

We normally don’t create derivatives for members because it can be very time consuming. However, sometimes we need access copies, especially before we send stuff to the Internet Archive.

 

To create derivatives we use MPEG Streamclip. To open it, go to the search bar on the upper right (it not always appears in the Applications folder because it’s a .dmg file that gets mounted every time we open the software). Go to: File > Open Files and select the video you want to transcode (you can also drag and drop).

 

You can also use Final Cut and Compressor, but I think MPEG Streamclip is good enough for the type of access copies we normally need.

 

 

 

 

 

 

 

 

 

 

 

 

 

Then go to File > Export to MPEG-4 (or whatever format you want).

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

Check settings and click on Make MP4.

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

** **

**2.**  	**Using MediaInfo**

 

Another Useful tool is MediaInfo, on the command line. This software shows technical information about a file, such as wrapper, video encoding, audio tracks, etc.

 

To use it, open Terminal. Then type *mediainfo *and drag and drop the video file. Then press enter… voilà! You will see all the info on the Terminal window.

 

 

 

Note: Don’t forget to add a space between the command and the file path!

 

 

 

 

 

 

 

 

 

