# Local Environment Setup

Use the following steps as an informal guide to setting up VS Code to run python and python notebooks.

## Pre-requisites
- Know how or desire to learn to program with Python :)

## Install and Configure

1. [Install **VS Code**](https://code.visualstudio.com/). This demo was created with [VS Code version 1.99](https://code.visualstudio.com/updates/v1_99) on Windows.

1. [Install python](https://www.python.org/downloads/). This demo was created with **Python 3.11.9**. The GraphRAG library required Python <3.13, >=3.10 at the time of this demo. Please check the "Requires" meta documented [on PyPi for GraphRAG](https://pypi.org/project/graphrag/) for the latest python version requirement. Be sure to add the python install directory to the PATH as part of the selected install options.

1. Most python packages come with **pip** pre-installed. If it is not installed, or to ensure you have the current version, run the below in a terminal window. See ["ensurepip"](https://pip.pypa.io/en/stable/installation/#ensurepip) for more information.

    ```
    python -m ensurepip --upgrade
    ```

1. There are 5 VS Code extensions recommended in the extensions.json file. If you are prompted to install recommended extensions, click the options to do so. If not, ensure the below extensions are installed and enabled on the **Extensions** panel (Ctrl + Shift + X): 

    - **Python** (Publisher: Microsoft)
    - **Python Debugger** (Publisher: Microsoft)
    - **Pylance** (Publisher: Microsoft)
    - **Jupyter** (Publisher: Microsoft)  (which will subsequently enable Jupyter Cell Tags, Jupyter Keymap, Jupyter Slide Show, and Jupyter Notebook Renderers)
    - **PowerShell** (Publisher: Microsoft)

## Create a Workspace Folder and Python Environment

1. Create a new folder on your local machine where you want to store your project files. You can do this outside of VS Code using your operating system’s file explorer.
1. Within VS Code **File** menu, select **Open Folder**. Navigate to the folder you created above and open it within VS Code.
1. Select **View** > **Command Palette**. Then type `Python: Create environment` and press **Enter**.
1. Select the **Venv** option.
1. Choose the python installation path from the above steps.
1. Select **Terminal** > **New Terminal**.
1. From the **Terminal** window, (typically on the bottom of your screen), click the `+` button and launch the **Command Prompt** terminal type.
1. Type the following to execute the virtual environment activate bat file script: `".venv\Scripts\activate"`.
1. Ensure that the terminal now shows a `(.venv)` prefix. 

## Use a requirements file to pip install ipykernel, which can be used to run python notebooks

1. In the **Explorer** panel (```Ctrl + Shift + E```), hover over the workspace header and click the **New File** icon to create a file. Name the new file `requirements.txt` and click **Enter**.
1. Add this text to line 1 in the file: `ipykernel==6.29.4`. Then, save the file (`Ctrl + S`).
1. In the **Terminal** window, you should have a cmd terminal that is showing the `(.venv)` prefix. Within this terminal, type `pip install -r ./vscode_python/requirements.txt` and press **Enter**.
    - It is finished when a new line appears prefixed with `(.venv)`.

## Test python files

1. In the **Explorer** panel (```Ctrl + Shift + E```), hover over the workspace header and click the **New File** icon to create a file within this folder. Name the new file `python-test.py` and click **Enter**.
1. Enter the text `print('hello world!')` into the file when it opens and save the file (`Ctrl + S`).
1. With the cursor inside of the file contents, on the upper right side of the file, click the **Run Python File** icon.
1. Examine the **Terminal** window and ensure you see `hello world!`. Triage if unsuccessful.

## Test python notebooks

1. In the **Explorer** panel (```Ctrl + Shift + E```), hover over the workspace header and click the **New File** icon to create a file. Name the new file `notebook-test.ipynb` and click **Enter**.
1. From within the ipynb file, select **View** > **Command Palette**. Then type `Notebook: Select Notebook Kernel` and press **Enter**. When prompted, select `Python Environment` and then select the option aligned with your virtual environment (e.g. `Python 3.** ('.venv': venv)`).
1. In the available cell, type `print('hello notebook!')`.
1. Click the **Execute cell** icon to the left of the cell to execute the cell's command. Ensure that `hello notebook!` prints in the cell output. Triage if unsuccessful.

## Cleanup 

Optionally, clean up any terminal windows opened. You can do this by clicking the barbage bin icon for each terminal window shown until the Terminal panel disappears. You can also issue a `clear` command to clear any previous commands from the window. 

Additionally, delete the test files:
- python-test.py
- notebook-test.ipynb

## Re-opening VS Code

If you close and re-open VS Code, you may need to re-activate the virtual environment. From a new Command Prompt terminal, you can use the following to activate your virtual environment: `.venv\Scripts\activate`.

[[Back to top](#local-environment-setup)]