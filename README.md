# Environment 
python\==3.6
tensorflow==2.0.0
## The structure of "code" folder
 - layers   # implementation of each layers
 - property.json  # a json file containing parameters, you can modify its content to optimize the model
 - requirements.txt  #the requirements file, use "**pip install** -r **requirements**. **txt**" to install all needed packages
 - train.py   # the main file to build and run our model
 - utils.py   # utility functions
 - run.sh    # a shell command to help you run the train.py file
 - data  # a folder containing all preprocessing related codes and data

## The structure of "data" folder

 - pop_fake_5348x51_20200123.csv   # raw csv data
 - preprocessing.py   # the preprocessing code
 - property.py   # the property used to determine meta-paths in preprocessing
 - run.sh   #the shell code to run preprocessing.py
 - Other pkl files are generated after preprocessing.

## How to run the code

cd code/data
./run.sh   ##preprocessing 
cd .\.
./run.sh   ## run the model


## How to run it on your own dataset

 1. Prepare your own csv file with raw data
 2. modify the filename in code/data/run.sh with you raw data location
 3. run code/data/run.sh
 4. modify the value of -g flag in code/data/run.sh based on how much pkl files are generated in the preprocessing step
 5. run code/run.sh
 6. try to change other parameters to optimize the model

## What's the meaning of other flags in the code?
Try to run "**python** **train.py** -h" or "**python** **preprocessing.py** -h", or look into the code, or ask me directly to get more information :)
