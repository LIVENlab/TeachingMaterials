# Welcome on board!

These are materials prepared for the course on [Green Engineering](https://guies.uab.cat/guies_docents/public/portal/html/2024/assignatura/44729/es), part of the [RICSE](https://www.uab.cat/web/estudiar/official-master-s-degrees/general-information-1096480962610.html?param1=1345875382068) master program at UAB. 
It is prepared by Cristina Madrid (cristina.madrid@uab.cat). 
Please leave your comments and suggestions in the [Issues](https://github.com/LIVENlab/TeachingMaterials/issues) section.

As we commented in class, [Brightway2.5](https://docs.brightway.dev/en/latest/ ) is a very powerful software ecosystem for LCA. It allows you to performed customized LCAs without the constraints of the commercial software. However, it is not as user-friendly as commercial software, and it requires some time to get used to it.

There is a great community of developers and users behind BW2.5, and they have prepared a lot of documentation and tutorials that can help you to get started. 


# Installing Brigthway2
**THIS STEP CAN TAKE YOU TO UP TO AN HOUR**

As indicated in the BW2 installation site, you first need to install a distribution of python. In this case we will use Anaconda:  https://docs.brightway.dev/en/latest/content/installation/index.html

As recommended by the BW25 community, we will update conda and install the [libmamba](https://www.anaconda.com/blog/a-faster-conda-for-a-growing-community) solver in the base environment. This is done by introducing the following commands in the anaconda prompt:

```
conda update -n base conda
conda install -n base conda-libmamba-solver
conda config --set solver libmamba
```
We are also going to install a package that will allow us to use the conda environment in Jupyter Notebook. This is done by introducing the following command in the anaconda prompt:
``` 
conda install -n base nb_conda_kernels
```

Once you have downloaded and installed anaconda, you need to open the anaconda prompt and use it to introduce the instructions for the BW25 installation.

We will create a new preconfigured Conda environment called ricse_bw25 with the configuration of the ricse_bw25.yml file. To do so, download the file `ricse_bw25.yml` from this repository and run the following command in the anaconda prompt:
```
conda env create -f <your_route/>ricse_bw25.yml
```
This will create a new environment called ricse_bw25. To activate it, run the following command:
```
conda activate ricse_bw25
```
**If you have a problem with the recognition of the conda commands after you activate the env, just use the anaconda navigator to open the anaconda prompt of ricse_bw25. Alternatively you can reinstall Jupter notebook with pip**
```
pip3 install notebook
```

As we are using a [Jupyter Notebook](https://jupyter.org/), you do not necessarily need to install [PyCharm](https://www.jetbrains.com/pycharm/), but you can do so if you want to, as PyCharm allows you to work with Jupyer Notebooks. Remember that you can get a free professional license for PyCharm(that will allow you to use Jupyter Notebooks inside) if you are a student [here](https://www.jetbrains.com/community/education/#students).

# Doing the exercises
If you installed the environment correctly, you should be able to open the Jupyter Notebook of this repository. To do this either:
* Run this code in the anaconda prompt (remember that your ricse_bw25 environment should be activated and that you need to be in the folder where the notebook is located):
```
cd <your_route_to_the_project_FOLDER>
jupyter notebook
```
You will see a new tab opening in your browser with the Jupyter Notebook in it. 

* Clone this repository in PyCharm (prof) and open the jupyter notebook from there.

