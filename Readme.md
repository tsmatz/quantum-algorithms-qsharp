# Quantum Algorithms in Q#

These examples show you quantum algorithm's implementation by Q# code.

For details about these algorithms, see [this series](https://tsmatz.wordpress.com/2019/02/21/quantum-computing-programming-qsharp-for-phase-kickback/) in my blog post.

- [Bernstein-Vazirani algorithm](./01-bernstein-vazirani.ipynb)
- [Grover's Algorithm (Black-box Search)](./02-grover-search.ipynb)
- [Quantum Phase Estimation (with Fourier Transform)](./03-phase-estimation.ipynb)
- [Quantum Arithmetic (Adder, Multiplier, and Exponentiation)](./04-arithmetic-operations.ipynb)
- [Shor's Algorithm (Quantum Period Finding)](./05-shor-period-finding.ipynb)

## How to set up quantum local simulator

By using Jupyter notebooks on Azure Quantum, you can develop and run Q# code without installing any additional tools.<br>
In this setting, we'll install Quantum Development Kit (QDK) on local machine (Ubuntu), and run Q# on local simulator.

1. Create Ubuntu Server 20.04 LTS virtual machine in [Azure Portal](https://portal.azure.com/).
2. Login to Ubuntu and check whether Python 3.8 is installed.<br>
```
python3 -V
```
3. Download Miniconda installer for Python 3.8 and install.<br>
(See [here](https://docs.conda.io/en/latest/miniconda.html) for the list of latest installers.)<br>
```
wget https://repo.anaconda.com/miniconda/Miniconda3-py38_4.12.0-Linux-x86_64.sh
bash Miniconda3-py38_4.12.0-Linux-x86_64.sh
```
4. Logout and login again to make the changes take effect.<br>
And, create conda environment with the following channel (additional packages).<br>
```
conda create -n qsharp-env -c microsoft qsharp notebook
```
5. Activate this environment. (Everytime you login to this local machine, please activate this environment.)<br>
```
conda activate qsharp-env
```
6. Run Jupyter notebook in this conda environment.<br>
```
jupyter notebook
```
7. Connect to Ubuntu server with SSH tunnel (port forwarding) from your working desktop in order to access notebook URL.
For instance, the following is the SSH tunnel setting on "PuTTY" terminal client in Windows. (You can use ```ssh -L``` option in Mac OS.)<br>
![SSH Tunnel settings with putty](https://tsmatz.github.io/images/github/azure-ml-tensorflow-complete-sample/20191225_SSH_Tunnel.jpg)
8. Copy the notebook URL (```http://localhost:8888/?token=...```) in the console output and open this address with your web browser.
9. Clone this repository and run each notebook in this repository.

*Tsuyoshi Matsuzaki @ Microsoft*
