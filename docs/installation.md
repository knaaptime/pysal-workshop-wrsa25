## Installation

We will be using a number of Python packages for geospatial analysis.



## Installing Miniforge

Miniforge is a minimal installer for Conda, a popular package and environment manager for Python and other languages. Here's how to install Miniforge on Windows and Mac:

### Windows

1.  **Download the installer:**

      * Go to the Miniforge GitHub releases page: [https://github.com/conda-forge/miniforge/releases](https://www.google.com/url?sa=E&source=gmail&q=https://github.com/conda-forge/miniforge/releases)
      * Download the latest "Miniforge3-Windows-x86\_64.exe" installer.

2.  **Run the installer:**

      * Double-click the downloaded installer file.
      * Follow the on-screen instructions. You can usually accept the default settings.

3.  **Verify the installation:**

      * Open a new command prompt or PowerShell window.
      * Type `conda --version` and press Enter. You should see the Conda version printed if the installation was successful.

### Mac

1.  **Download the installer:**

      * Go to the Miniforge GitHub releases page: [https://github.com/conda-forge/miniforge/releases](https://www.google.com/url?sa=E&source=gmail&q=https://github.com/conda-forge/miniforge/releases)
      * Download the latest "Miniforge3-MacOSX-x86\_64.sh" installer.

2.  **Run the installer:**

      * Open a terminal window.
      * Navigate to the directory where you downloaded the installer.
      * Make the installer executable: `chmod +x Miniforge3-MacOSX-x86_64.sh`
      * Run the installer: `bash Miniforge3-MacOSX-x86_64.sh`
      * Follow the on-screen instructions. You can usually accept the default settings.

3.  **Verify the installation:**

      * Close and reopen your terminal window to ensure the changes to your shell configuration take effect.
      * Type `conda --version` and press Enter. You should see the Conda version printed if the installation was successful.

**Additional notes:**

  * **Choosing the right installer:** Make sure to download the installer that matches your operating system (Windows or macOS) and architecture (x86\_64 for most modern systems).
  * **Alternative installers:** If you need a different version of Python or a specific architecture, you can find other installers on the Miniforge releases page.
  * **Conda-forge:** Miniforge is configured to use the `conda-forge` channel by default, which provides a wide range of community-maintained packages.
  * **Troubleshooting:** If you encounter any issues, refer to the Miniforge documentation or seek help from the Conda community.

After installing Miniforge, you'll have access to the `conda` command, which you can use to create environments, install packages, and manage your Python projects.


Start a terminal and navigate to the directory of the downloaded/ cloned materials. For example, if the materials now live in the directory `/Users/knaaptime/Downloads/workshop-pysal-narsc` , you need to navigate to that directory from the terminal (using command `cd` ):

Once we have done that, run:

``` bash
mamba env create -f environment.yml
```

This will build a conda python  environment that sandboxes the installation of the required packages for this workshop so we don't break anything in your computer's system Python (if it has one).

This may take 10-15 minutes to complete depending on the speed of your network connection.

Once this completes, you can activate the workshop environment with:

``` bash
mamba activate workshop-pysal
```

Then start jupyter

```bash
jupyter lab
```

You're now all setup for the tutorial!

## Troubleshooting

If you encounter the following error when starting jupyterlab:

``` bash
FileNotFoundError: [WinError 2] The system cannot find the file specified
```

A solution is to issue the following command in the anaconda prompt:

``` bash
 python -m ipykernel install --user
```
