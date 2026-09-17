# AI-Toolkit-ROCm
We expanded on AI toolkit to add general support for ROCm 7.2 based lora training.

Tested on Ubuntu 24 LTS with XFX AI Pro R9700

** Known bug **

Some of the 8 bit optimizers cause the image to turn to white noise after saving a step.  For example if your training run is 900 steps and your setting is to save after 300 steps, the image will turn to white noise on step 301.

Either use a 16 bit optimizer like Adamw or do not save steps (set the "save after" number to be higher than the number of training steps).  EG, If there's 600 training steps, set the "save every x steps" to be greater than 600 to avoid the bug.
