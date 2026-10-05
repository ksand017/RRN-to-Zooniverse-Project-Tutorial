# This tutorial will show you how to upload "subject sets" from the Roman Research Nexus (RRN) to a Zooniverse project using Panoptes
- [Zooniverse](https://www.zooniverse.org/) is the worlds largest and most widely used platform for hosting people-powered research projects (citizen science)
- The [Panoptes](https://panoptes-python-client.readthedocs.io/en/latest/index.html) package allows you to manage Zooniverse projects through python
- A [Subject](https://help.zooniverse.org/getting-started/#subjects) is a unit of data to be classified or analyzed.
- A [Subject set](https://help.zooniverse.org/getting-started/#subject-sets) is a group of data units (images), along with their metadata ("manifest").  
- More information on getting started with Zooniverse can be found [here](https://help.zooniverse.org/getting-started/)

### In this tutorial, you will learn how to 
- 📡 connect to Zooniverse from within a python environment on the RRN using Panoptes
- 📁 create a new project linked to your Zooniverse account
- 🌠 create a new subject set and link subjects to the project

This tutorial only covers uploading subject sets from the RRN to Zooniverse, and assumes the user has already created subject set images that are stored on the RRN or externally. 

After completing this tutorial, you can then login on the Zooniverse.org side and create a workflow, which is a series of tasks (questions or drawing tasks) that you would like people to complete for each subject in your project. 

### Installing panoptes_client
The panoptes_client does not come pre-installed on the RRN. To install the panoptes_client package, you will need to [create a new python environment](https://roman.science.stsci.edu/user/ksand017/lab/tree/references/roman_notebooks/markdown/software.md) on your RRN account. Then you can install panoptes by following [these instructions](https://panoptes-python-client.readthedocs.io/en/latest/user_guide.html#installation). You will also need to install pandas, astropy, tqdm, and fastparquet: ```pip install panoptes_client pandas astropy tqdm fastparquet```
