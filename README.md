## HungryAI - Readme.md
Thanks for taking the time to check out my HungryAI project! This project is about experimenting with GANs by seeing if they can generate images of things they have never seen before. 

Check out “HungryAI - Final Report” to learn about my project from a big picture standpoint.

If you want a more in depth description of how I conducted the experiment and wrote the code for it, check out “hungry_ai.ipynb” as well as the other bits of code mentioned in “Alder’s Code Organization” below. 

Special thanks to Humphrey Shi and Steven Walton! They taught my CS 472 “Machine Learning” class at the University of Oregon. I wouldn’t have been able to make this project without their help and instruction. 

## Alder’s Code Organization
1. text2image-alder/hungry_ai.ipynb - This jupyter notebook walks through the different steps of my experiment, from dataset preparation to model training and testing. 
    a. NOTE: I was having trouble training the text encoder and SSAGAN from directly within the Jupyter notebook, so instead I ran the commands to train them from “Windows Powershell”. I mention this within the notebook, but I just wanted to clarify why these important processes are omitted from the notebook. 

2. text2image-alder - This folder contains the source code to build and train my SSAGAN model. It is a copy of the “https://github.com/wtliao/text2image” repo that I modified to work with my dataset. Doing so took a significant amount of work, mostly within the files main.py and datasets.py. If you search these files for “Alder” you should see a significant amount of comments describing the changes I made. 

3. DAMSM/Style-AttnGAN-master - This folder contains the source code to build and train the text encoder for my SSAGAN model. It is a copy of the “https://github.com/sidward14/Style-AttnGAN” repo that I modified to work with my dataset. Doing so took a fair amount of work, mostly within the files pretrain_DAMSM.py and datasets.py. If you search these files for “Alder” you should see a significant amount of comments describing the changes I made. 

4. DATASETS - I am choosing not to upload my food combination images dataset to Github because it’s too large to upload and store there. FYI, my datasets were set up similarly to the CUB dataset, with a root “images” folder, then a folder for each class within this root folder, and the images for each class within these class folders. For my “text” dataset, i.e. the dataset of all my captions, I wrote a .txt file with 10 captions per image, with the same path and file name as the images (so in the class folders), except ending in .txt. That way I could easily load the captions by using logic similar to that in datasets.py. 
