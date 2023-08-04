# python-selenium-tutorial
## Install Python and pip:
Python should come pre-installed on Ubuntu 22.04. However, you can ensure it's installed by running:

````
sudo apt install python3 python3-pip1
sudo apt install python-is-python3
````

## Install Chrome web browser:
If Chrome is not installed on your system, you can do so by running the following 
````
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt update
sudo apt install google-chrome-stable
````
## Check the Chrome version:
After installing Chrome, check its version. Ensure the version matches the ChromeDriver version later on:

````
google-chrome --version
````
## Download and install ChromeDriver:
Next, you need to download and install ChromeDriver. Make sure to replace <chrome_version> with your installed Chrome version (e.g., 94.0.4606.61).

````
CHROME_DRIVER_VERSION=<chrome_version>
wget -N https://chromedriver.storage.googleapis.com/${CHROME_DRIVER_VERSION}/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
chmod +x chromedriver
sudo mv chromedriver /usr/local/bin/
````
## Install Selenium:
Now, you can install the Selenium library for Python using pip:

````
pip3 install selenium
````
## Install Pycharm:
Now, install the Pycharm Code Editor:

````
snap find pycharm #find pycharm vesion
snap install pycharm-community --classic
````
Then open pycharm and select ``` Do not import settings ```

## Verify the setup:
To verify that everything is working correctly, you can create a simple Python script and run it. Here's an example:

* Open Pycharm  Click on ``` New Projct ``` give Project Name and select your custom location then click on `` create ``
* Select On `` file `` then go to `` Settings `` select ``` Python interperator ``` click on Plus sign ``` + ``  Seacrh ``` selenium ``` and install selenium package last of all ok all window .
* Create Python file(test_selenium.py)  Add below code:
````                                                                                                                                                           
from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://www.google.com")
````
Save this script (e.g., test_selenium.py) and run it using Python:
```
python test_selenium.py
```

If everything is set up correctly, a new Chrome browser window should open, and it should navigate to the Google homepage.
