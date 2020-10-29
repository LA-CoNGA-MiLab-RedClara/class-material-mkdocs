# 13 TeV ATLAS Open Data virtual machine installation

**Download the latest ATLAS Open Data VM**

[![download](pictures/download_vm.png)](https://zenodo.org/record/3687320/files/ATLAS-Open-Data-ubuntu-2020-v4.ova)

This is an **Ubuntu 18.04.3 LTS** with:

* **ROOT** 6.18 (configuration all)

* **Jupyter** (bash, python2, python3, ROOT C++ kernels)

* **Extras** TensorFlow + demo git repos

* **Cite with** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3629875.svg)](https://doi.org/10.5281/zenodo.3629875)

<hr>

**Check our ~9 min video tutorial to don't miss any detail**

<iframe scrolling="no"  src="https://videos.cern.ch/video/OPEN-VIDEO-2020-018-002" width="100%" height="420" frameborder="0" allowfullscreen></iframe>


<hr>

## Detailed instructions

+ After you downloaded the VM file, start the VirtualBox. Go to the menu ***"File"*** **->** ***“Import Appliance...”*** (or perform the same function with the combination of buttons: **"Ctrl" + "I"**).

![path](pictures/fig-7-1.png)

+ In the window, select the downloaded ".ova" file from the **Downloads** folder and click "Next":

![path](pictures/fig-7-2.png)

+ Click "Import" without any changes:

![path](pictures/fig-7-3.png)

+ The operating system should begin importing:

![path](pictures/fig-7-4.png)

— Now your Virtual Machine with Ubuntu-Linux operating system is ready, start it by clicking ![path](pictures/fig-7-5.png) and use:

![path](pictures/fig-7-6.png)

<hr>
**Download the latest ATLAS Open Data VM**

[![download](pictures/download_vm.png)](https://zenodo.org/record/3687320/files/ATLAS-Open-Data-ubuntu-2020-v4.ova)

This is an **Ubuntu 18.04.3 LTS** with:

* **ROOT** 6.18 (configuration all)

* **Jupyter** (bash, python2, python3, ROOT C++ kernels)

* **Extras** TensorFlow + demo git repos

* **Cite with** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3629875.svg)](https://doi.org/10.5281/zenodo.3629875)


<hr>

# Previous VM demo on how to run the VM

**Take a look to this video on how to get and run some notebooks and framework in your computer**

<CENTRE>
<iframe width="100%" height="405" src="https://www.youtube.com/embed/Lj73Vjd6Nys?start=52" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</CENTRE>

<hr>

_ _ _
N.B. If you want to install your operating system (in this case Ubuntu) from scratch, then see how to do it in [***this section***](appendix.md).
_ _ _


<!--


After starting your VM and running the notebooks, you may encounter the following **error** (look at the red frames in the photo below):

![path](pictures/fig-12-3.png)

To solve this **error**, follow these simple steps:

+ Сlose notebooks and terminal

+ Run the terminal again and type the following code: * `./run-server-jupyter.sh` * to start Jupiter

![path](pictures/fig-12-4.png)

+ This way you have restarted your terminal and server successfully

![path](pictures/fig-12-5.png)

+ Open the notebook in your browser and restart the *kernel* by clicking the restart button

![path](pictures/fig-12-6.png)

+ Now your terminal and server should be working and the notebooks should run without errors

![path](pictures/fig-12-7.png)
-->
