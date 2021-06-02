# Gerlich Jupyter
Our base container with all internally used NGS and image analysis tools preinstalled.

# VBC JupterHub

You can run use this container on ```https://jupyterhub.vbc.ac.at/```.
To set it up use the following settings:
![Jupyterhub Settings](images/settings.png)
You change the version by changing the image URL past the double colon:
`.../gerlichlab/jupyter-gerlich:YOUR_FAVORITE_VERSION`

or <span style="color:red">**copy and past the link from the version subsection bellow.**<span>

Once the server is started do not choose a specific kernel rather choose the basic Python3 kernel.
![Python Kernel](images/kernel.png)
It will contain everything installed in the container.

# Running the notebook locally (OPTIONAL)
For your convenience, you can then start a notebook server with all the necessary libraries installed with:
```docker-compose up``` from the command line in the repo directory.
Then just open up a browser and navigate to http://localhost:9999 or http://localhost:9999/lab for the jupyter lab interface. 
This will prompt you for a password, which was disclosed in the python club lecture.

If you use this setup more regularly, please change the password in the jupyter_notebook_config.py

# Connecting the local notebook to VSCode 
A brief description by Michael can be found [here](https://github.com/gerlichlab/python_club_seq_formats_I).

# Versions
## Version 1.0
Base version.

Singularity image URL: `https://singularity.vbc.ac.at/v1/imagefile/library/gerlichlab/jupyter-gerlich:version-1.0`
# How do I get a custom version
 
- Create a new branch
- Modify the gerlich_base.yml (e.g., add all your missing libraries or change the version of the libraries)
- Test your build by running: `docker-compose -f docker-dev.yml up`
- Test your notebook in the browser: http://localhost:9999
- Pushing your branch will create a pull request. Add a description for your version and including what is different to the base version and why it was created. This can be extended and modified on the github homepage.
- Contact Christoph or Michael, we will give it a new version number and make it available on jupyterhub.vbc.ac.at
