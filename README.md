# Basic Pandas and Numpy Course for Non-Tech Colleagues

## 1. Introduction to Python, venv, and Jupyter Notebooks
- **Overview of Python Programming**
- **Introduction to virtual environments in Python**
- **Introduction to Jupyter Notebooks**
  - Explanation of how they work and their importance in data analysis.
- **Activities:**
  - Install Python and Jupyter Notebook.
    - Provide step-by-step instructions, including the use of `pip` for installing packages.
  - Create a simple Python script to demonstrate basic syntax.

## 2. Introduction to Pandas
- **Understanding DataFrame and Series**
- **Data Import/Export Using Pandas**
- **Basic Data Manipulation**
  - Filtering, sorting, grouping.
- **Activities:**
  - Practical exercises with real-world datasets.

## 3. Fundamentals of Numpy
- **Basic Concepts of Arrays and Matrix Operations**
- **Common Functions and Their Uses**
- **Activities:**
  - Array creation, manipulation, and basic operations exercises.

## 4. Data Cleaning and Preparation
- **Handling Missing Data**
- **Data Transformation Techniques**
- **Activities:**
  - Apply techniques on a slightly dirty dataset for analysis preparation.

## 5. Basic Data Analysis and Visualization
- **Descriptive Statistics Using Pandas**
- **Introduction to Data Visualization**
  - Using Matplotlib and Seaborn.
- **Activities:**
  - Analyze a dataset for patterns and anomalies.
  - Create basic plots (line, bar, scatter, histogram).

## 6. Introduction to Predictive Analytics
- **Overview of Predictive Analytics and Applications**
- **Simple Linear Regression**
- **Activities:**
  - Build and interpret a simple predictive model.

## 7. Course Project
- **Objective:**
  - Apply learned concepts in a comprehensive project.
- **Guidance:**
  - Select a dataset.
  - Perform end-to-end analysis (cleaning, exploration, visualization, predictive modeling).

## 8. Additional Resources
- Links to online resources, tutorials, and forums.

## 9. Feedback and Evaluation
- Collect feedback for course improvement.
- Conduct tests or quizzes for learning evaluation.

_____________________________
# How to Install Python

## Step 1: Download Python
1. Visit the official Python website: [python.org](https://www.python.org/).
2. Go to the Downloads section. The website will suggest the best version for your operating system (Windows, MacOS, Linux/UNIX).
3. Click on the download link for the latest version.
4. After the download completes, locate the installer file in your downloads folder.

## Step 2: Run the Installer
1. Double-click on the downloaded file to run the installer.
2. **Important**: At the start of the installation process, ensure to check the box that says **"Add Python 3.x to PATH"**. This step is crucial as it allows you to run Python from the Command Prompt or Terminal. In case you did not add it to PATH during installation, follow the ***"How to Manually Add Python to PATH"*** instructions 
3. Proceed with the installation by choosing either the default settings or customizing as per your needs.

## How to Manually Add Python to PATH

If you didn't add Python to your PATH during the installation or need to add it manually for any reason, follow these steps:

## For Windows

### Step 1: Locate Python Installation
1. Find where Python is installed. Default locations are usually:
   - `C:\Users\YourUsername\AppData\Local\Programs\Python\Python39\`
   - `C:\Python39\`
   Note: Replace `39` with your Python version number.

### Step 2: Add Python to PATH
1. Right-click on 'This PC' or 'My Computer' on your desktop or in File Explorer.
2. Select 'Properties'.
3. Click on 'Advanced system settings'.
4. In the System Properties window, click on the 'Environment Variables' button.
5. In the Environment Variables window, under the 'System variables' section, find and select the 'Path' variable, then click 'Edit'.
6. In the Edit Environment Variable window, click 'New' and add the path to your Python installation folder.
7. Add the `Scripts` folder path as well, typically found within your Python installation directory (e.g., `C:\Python39\Scripts`).
8. Click 'OK' to close each window.

### Step 3: Confirm Python is in PATH
1. Open Command Prompt.
2. Type `python --version` and press Enter. If Python is in your PATH, you'll see the Python version.
3. Type `pip --version` to check if pip is also accessible.

## For MacOS/Linux

### Step 1: Open Terminal
1. Open Terminal.

### Step 2: Edit Profile File
1. Type `nano ~/.bash_profile` for Bash or `nano ~/.zshrc` for Zsh, and press Enter. (Depends on your shell)
2. Add the following line at the end of the file:
   ```bash
   export PATH="/path/to/python:$PATH"

## Step 3: Verify Installation
1. After installation, open Command Prompt (Windows) or Terminal (MacOS/Linux).
2. Type the following command and press Enter:
   ```python
   python --version

3. You should also verify the installation of pip (more on pip later). Type the following command and press Enter:
    ```python
   pip --version
________________________
## 1. Setting Up a Virtual Environment (venv)
- **Why Use a Virtual Environment?**
  - Isolates project dependencies.
  - Prevents conflicts between different projects.
- **Creating a Virtual Environment**
  - Open Command Prompt (Windows) or Terminal (MacOS/Linux).
  - Navigate to your project directory.
  - Run the following command to create a virtual environment:
    ```sh
    python -m venv myenv
    ```
  - Replace `myenv` with your desired environment name.
- **Activating the Virtual Environment**
  - On Windows:
    ```sh
    myenv\Scripts\activate
    ```
  - On MacOS/Linux:
    ```sh
    source myenv/bin/activate
    ```
- **Installing Required Packages**
  - Once the virtual environment is activated, install necessary packages using `pip`:
    ```sh
    pip install pandas numpy jupyter
    ```
- **Deactivating the Virtual Environment**
  - To deactivate the virtual environment, simply run:
    ```sh
    deactivate
    ```
________________________
# Installing Jupyter Notebooks Using Pip and Getting Started

After installing Python, the next step in our course is to install Jupyter Notebooks, a powerful tool for interactive computing and data visualization.

## What is Jupyter Notebook?
Jupyter Notebook is an open-source web application that allows you to create and share documents containing live code, equations, visualizations, and narrative text. It's an essential tool for data analysis, data visualization, and scientific computing.

## Step 1: Install Jupyter Notebook
1. Open your Command Prompt (Windows) or Terminal (MacOS/Linux).
2. Install Jupyter Notebook using `pip`, Python's package manager, by typing the following command:
   ```python
   pip install notebook

3. Wait for the installation to complete.

## Step 2: Launch Jupyter Notebook
1. In the same Command Prompt or Terminal window, launch Jupyter Notebook by typing:
   ```python
   jupyter notebook

2. This command starts the Jupyter Notebook server and opens it in your default web browser.
3. Finding Jupyter's Portal if It Doesn't Open Automatically
   *  If Jupyter Notebook does not open automatically in your browser, you can manually access it.
   *  In the Command Prompt or Terminal, you will see a message like "The Jupyter Notebook is running at: http://localhost:8888/"
   *  Copy the URL (`http://localhost:8888/` or a similar one provided in your Command Prompt or Terminal).
   *  Paste this URL into your web browser's address bar and press Enter.
   *  This should take you to the Jupyter dashboard.
## Step 3: Explore Jupyter Notebook
1. The Jupyter dashboard will open in your browser, showing the contents of your current directory.
2. Create a new notebook by clicking the 'New' button at the top right and selecting 'Python 3' (or your installed Python version).
3. This action opens a new notebook where you can write and execute Python code in interactive cells.
4. Execute the code in a cell by pressing `Shift + Enter`.

## Step 4: Open an Existing Notebook
1. To open an existing notebook, navigate to the notebook's location in the Jupyter Dashboard.
2. Click on the notebook file (.ipynb) to open it in a new tab for editing and running code cells.

Jupyter Notebooks are incredibly versatile, allowing for a mix of code, text, and other multimedia resources. This makes it a great tool for learning and demonstrating Python, especially for data-related tasks.

## Going forward, this guide will continue in Jupyter notebooks.
``
