Brain EEG data readme
=====================

* brainvisionio.py - replacement file for the one in the neo library. The library has an error, and I had to manually fix them, so this file contains the corrections.
* intervals.txt = file which contains the time in ms where each picture was shown
* Untitled1.ipynb - file for use with `ipython notebook` which contains commands to load EEG data from only 64 channels/nodes, and calculate the average signal for each image for every channel/node.

# Getting Started for the first time

How to read data from .eeg file:

For the first time, you will need a virtualenv. To create it, go to the desired directory, and type in:

	virtualenv venv

This will create a workspace for you to work in.

Once installed, everytime you want to activate it, navigate to the direcory where `venv` is, and type:

	source venv/bin/activate

Once activated, you can start working. 

Make a directory for the project, and initialize git:

	git init

Once that is done, you need to do:

	git remote add origin git@github.com:waleedasif322/Brain-EEG-data-Viz.git

Pull the latest code from GitHub. Now you need to copy the .EEG file and the .VHDR file I gave you on your flash drive in the new project folder.

Once you have pulled, you need to install the dependencies.

	pip install -r requirements.txt

Since there is an error with the offical library that we use to read the binary data, you need to copy the file `brainvisionio.py` that you see in the folder, and replace it with the one that was installed by `pip`.

To do that, navigate to the folder where `venv` is located. Then type:

	cd /venv/lib/python2.7/site-packages/neo/io

You might have to modify this command if your python version is different.

Once you are in the `io` directory, replace the `brainvisionio.py` file with the one that I gave you in the original folder.

Once that is done, you can go back to the directory of the project. Once you are back, you can run:

	ipython notebook

This will  make it easier to work with the data.

Then load the file `Untitled1.ipynb`. Execute the commands from top to bottom.
The script will take about 1GB of ram on your PC, so make sure you close other programs.

The code will probably crash at the end since I am still working on that right now.


