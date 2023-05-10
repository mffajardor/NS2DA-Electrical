# Final Project -- Network Science for Data Analytics
## Analysis of an Electric Power System using Network Science Notebook

### Group 4 -- Members:
- Daniel Dario Fula
- Manuel Fajardo
- Laura Garzon

## Project Goals
The purpose of this project is to perform an analysis of an electric network using complex network analysis (CNA) techniques to identify key parameters, such as centrality analysis, betweenness centrality, and community detection. The goal is to determine optimal locations for deploying microgrids within electrical distribution systems and identify the most vulnerable nodes or links in the network. These findings will facilitate conducting various tests, such as loss of lines and substations, using simulators like MATPOWER or PandaPower in Python. This work utilizes the IEEE 118 bus test system, as detailed in our dataset and implemented network science approach sections.



### Limitations and Scope
The project’s limitations include the exclusion of analyses such as node embedding or similarity algorithms, which are not justified for the network type and application. Moreover, this analysis is not designed for networks with large numbers of nodes and edges, as their complexity could render the applied methods inapplicable to such systems. The project focuses on analyzing the IEEE 118 bus test system and implementing complex network analysis techniques to identify optimal locations for microgrids and vulnerable network components.

![Diagrama](IEEE118_Pandapower_Plotly.png)


## Instructions for use
### Google Colab
To use this notebook in Google Colab, open an empty Colab notebook. Now click in File and 'Open notebook', then click on the 'Github' button, where it says "Enter a GitHub URL or search by organization or user" put the URL of the repository "https://github.com/mffajardor/NS2DA-Electrical" and select the notebook. Then create a copy of the notebook (File => Save a copy in Drive). Install the necessary packages by running the following command in a new cell:

```python
!pip install pandapower py4cytoscape
```

![Colab](Google_Colab_step.png)

### Local Setup with Conda

If you wish to run this notebook on your local machine, you should have [Anaconda](https://www.anaconda.com/download#downloads) installed. After installing Anaconda, follow these steps to create a new Conda environment and install the necessary packages:

1. Open the Anaconda Command Prompt (Windows) or Terminal (Linux/MacOS).

2. Create a new Conda environment with Python 3.10:

```bash
conda create --name network_env python=3.10
```

3. Activate the Conda environment:

```bash
conda activate network_env
```

4. Install the necessary packages:

```bash
conda install -c conda-forge notebook pandas numpy plotly networkx
pip install pandapower[all] --upgrade
pip install py4cytoscape
```
If you encounter issues with the installation of pandapower[all], you can try installing the missing dependencies with:

```bash
sudo apt-get install libpq-dev python-dev
pip install psycopg2-binary
```

5. Navigate to the directory that contains the notebook and launch Jupyter Notebook:


```bash
cd /path/to/your/notebook/directory
jupyter notebook
```

### Visual Studio Code Setup with Conda

Install Visual Studio Code if you haven't done so already. You can download it from [here](https://code.visualstudio.com/download). If you want to use Visual Studio Code to work with Jupyter Notebooks, follow these additional steps:

1. Open Visual Studio Code.

2. Open the notebook file (.ipynb) in Visual Studio Code.

3. In the top right corner, select "Select Kernel".

4. Choose "Python Environments" and select the virtual environment you created (network_env).

You are now ready to run the notebook in Visual Studio Code.

If you encounter issues finding conda in Linux, you can resolve this by adding the path to your .bashrc or .zshrc file (depending on your shell):

```bash
echo "export PATH=/path/to/anaconda3/bin:$PATH" >> ~/.bashrc
source ~/.bashrc
```

Note: Replace /path/to/anaconda3/bin with the actual path to your Anaconda bin directory.

If you are using zsh and cannot find conda, execute the following command in your terminal:

```bash
eval "$(/home/mffajardor/anaconda3/bin/conda shell.zsh hook)"
```


## Use the file environment.yml with the libraries

## Installation

To install the required libraries, you'll need to have [Anaconda](https://www.anaconda.com/download#downloads) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) installed. 

Once you have Anaconda or Miniconda installed, navigate to the project's root directory and run the following command to create a new conda environment with the necessary libraries:

```bash
conda env create -f environment.yml
```

After the new environment is created, activate it with:

```bash
conda activate myenv
```

Now you're ready to run the Jupyter notebook:

```bash
jupyter notebook
```

Or use Visual Studio code [VSCode](#visual-studio-code-setup-with-conda) 

```bash
code .
```


