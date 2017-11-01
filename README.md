# test_training_py
# test_training_py
geckodriver-v0.19.0-linux32.tar.gz
wget https://github.com/mozilla/geckodriver/releases/download/v0.19.0/geckodriver-v0.19.0-linux32.tar.gz
tar -xvzf geckodriver*
chmod +x geckodriver
sudo mv geckodriver /usr/local/bin/

======virtual screen============================================================
pip install pyvirtualdisplay selenium
You might need xvfb too:

sudo apt-get install xvfb
Then try adding this code:

from pyvirtualdisplay import Display
display = Display(visible=0, size=(800, 600))
display.start()
Full example:

from pyvirtualdisplay import Display
from selenium import webdriver

display = Display(visible=0, size=(800, 600))
display.start()

browser = webdriver.Firefox()
browser.get('http://www.python.org')

browser.close()
display.stop()
================================================================================
sudo firefox

setp 1: install Xvfb
apt-get install Xvfb

setp 2: run Xvfb
nohup sudo Xvfb: 10 - ac &

step 3: set the terminal 
export DISPLAY=:10
================================================================================
