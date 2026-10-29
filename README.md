# This tutorial will show you how to upload "subject sets" from the Roman Research Nexus (RRN) to a Zooniverse project using Panoptes
- The [RRN](https://roman-docs.stsci.edu/data-handbook/roman-research-nexus) is a cloud based environment provided by the Space Telescope Science Institute (STScI) for analyzing data from the Roman Space Telescope. 
- [Zooniverse](https://www.zooniverse.org/) is the worlds largest and most widely used platform for hosting people-powered research projects (citizen science).
- The [Panoptes](https://panoptes-python-client.readthedocs.io/en/latest/index.html) package allows you to manage Zooniverse projects through python.
- A [Subject](https://help.zooniverse.org/getting-started/#subjects) is a unit of data to be classified or analyzed.
- A [Subject set](https://help.zooniverse.org/getting-started/#subject-sets) is a group of data units (images), along with their metadata ("manifest").  
- More information on getting started with Zooniverse can be found [here](https://help.zooniverse.org/getting-started/).

### In this tutorial, you will learn how to 
- 📡 connect to Zooniverse from within a python environment on the RRN using Panoptes
- 📁 create a new project linked to your Zooniverse account
- 🌠 create a new subject set and link subjects to the project

This tutorial only covers uploading subject sets from the RRN to Zooniverse, and assumes the user has already created subject set images that are stored on the RRN or externally. 

After completing this tutorial, you can then login on the Zooniverse.org side and create a workflow, which is a series of tasks (questions or drawing tasks) that you would like people to complete for each subject in your project. 

## Getting started
### Create Zooniverse Account
Navigate to [https://www.zooniverse.org/](https://www.zooniverse.org/) and click register in the top right corner to create an account.

### Access the Roman Research Nexus with a MyST account
Anyone with a Space Telescope Science Institute (STScI) [MyST account](https://proper.stsci.edu/proper/authentication/auth) can launch a [Roman Research Nexus](https://roman.science.stsci.edu/hub/) session. 

### Installing panoptes_client
The panoptes_client does not come pre-installed on the RRN. To install the panoptes_client package, you will need to create a new python environment (in the RRN select "Installing Extra Software" from the intro markdown file, or navigate to references/roman_notebooks/markdown/software.md) on your RRN account. Then you can install panoptes by following [these instructions](https://panoptes-python-client.readthedocs.io/en/latest/user_guide.html#installation). You will also need to install pandas, astropy, tqdm, and fastparquet: ```pip install panoptes_client pandas astropy tqdm fastparquet```

Alternatively, you can setup the new python environment using the provided YAML file. To do this from the terminal, change directory (cd) to the location of the repository contents and run ```kernel-create rrn-2-zooniverse-env rrn-2-zooniverse-specs.yaml "RRN-2-Zooniverse-env"```