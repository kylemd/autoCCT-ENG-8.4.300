# Instructions

To use this script, you will need **Python** at least version 3.6.0 and **pip**

Go to https://www.python.org/downloads/ to download and install Python

Next, use the command line to install pip:

**curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py**

**python get-pip.py**

To install requirements, use the command:
  
  **pip install -r requirements.txt**
  
Run the script with the command:
  
  **python autoCubes.py**
  
Add keys with a space after them, if necessary. For example:

  **python autoCubes.py --gcam**
  
  or
  
  **python autoCubes.py --nophone --debug --showpoints --nowb**

  
Before you start calibrating, make sure you shoot the target under the necessary white balance conditions.

Connect your phone via adb (attached) and authorize it, if not done before, to automatically load photos from your phone.

If there is an adb related error on startup and you are sure the phone is connected, check to see if adb is already running and terminate it in the task manager. 

Or use the **--nophone** key to use local photo. By default the local photo is found in the folder where the script is located and named last_photo.jpg

If you want to specify a different file, you can send the file name to the script, e.g. 
  
  **python autoCubes.py --nophone some_photo.jpg**

(If you calibrate from a photo without a phone, you can't use matrix refinement because you have to take a photo with a calculated matrix to do that)

If you are going to use one sensor (Google Camera), take the picture under neutral light (daylight, daylight bulb)

Shoot the color target so that the white square of the target is on the left.

It does not matter if it is horizontal or vertical.

For Gcam (Google Camera) add the key **--gcam**

For x-rite checker add key **--xrite**

If you are calibrating two matrices/cubes for warm or cold temperatures, the warm matrix is calibrated by default.

To calibrate cold, add the key **--cool**

For two matrices, add **--matrixes**

(correctly matrices, but some talented developers have problems with English)

For a cube, add **--cube**

For cubes add **--cubes**.


If you shoot with a PhotonCamera and your phone is adb-connected, 
it will automatically calibrate the sensor for calibration.

If you are shooting with a Google Camera with CCT, before calibrating, turn off the color settings and set the sensor as follows:

RR: 1 RG: 0 RB: 0

GR: 0 GG: 1 GB: 0

Br: 0 BG: 0 BB: 1
