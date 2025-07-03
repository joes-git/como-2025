# Instructions for the AIHEP Como school tutorials 2025

To successfully follow along with the tutorials we highly recommend the following:

- A laptop with 10-20 GB of free storage, running either Linux or Mac OS. If you can only use Windows, make sure you have [WSL prepared](https://learn.microsoft.com/en-us/windows/wsl/install).
- Python 3.10, 3.11 or 3.12
- A working installation of LHAPDF, tensorflow and numpy.

The following instructions will guide you through the installation of conda and all necessary packages to successfully follow the tutorials.

1. Install the right version of conda depending on your system: https://www.anaconda.com/docs/getting-started/miniconda/install#macos-linux-installation

    Note: for WSL you need to use the Linux Terminal Installer instructions
  
    Alternatively, the following script will try to automatically download the right version:
    ```
    curl https://raw.githubusercontent.com/NNPDF/binary-bootstrap/master/bootstrap.sh -o bootstrap.sh
    sh bootstrap.sh
    ```

2. Once you have installed conda and activated it, please run the following command to create an environment specifically for the school tutorials:
    (remember to change `$HOME/miniconda3` to the path of your conda installation if you modified the default)

    ```
    source $HOME/miniconda3/bin/activate
    conda create -n env_como -c conda-forge --override-channels 'python<3.13' lhapdf pineappl==0.8.6 eko jupyterlab matplotlib pandas tensorflow -y
    conda activate env_como
    ```

    NOTE: the last command, `conda activate env_como`, needs to be run every time you open a new terminal!

3. For some of the tutorials you might need other packages

    for QCD (1st week);
    ```
    conda activate env_como
    python -m pip install yadism
    ```

    for Quantum Computing (2nd week) you will need an isolated environment:
    ```
    conda create -n quantum_env 'python<3.13' jupyterlab
    conda activate quantum_env
    python -m pip install qibo qiboml
    ```

Now run `jupyter lab` and enjoy :)

Make sure you can import packages such as `lhapdf`, `tensorflow`, and `pineappl` from your notebook: https://docs.jupyter.org/en/latest/

## Common issues

- If you cannot import the packages `lhapdf`, `tensorflow`, or `pineappl` in your notebook, while you can do so in the terminal, you might need to install the Jupyter kernel for your conda environment. Run the following command:

    ```
    python -m ipykernel install --user --name env_como --display-name "Python (env_como)"
    ```
  Restart Jupyter Lab and select the kernel "Python (env_como)" from the Kernel menu.