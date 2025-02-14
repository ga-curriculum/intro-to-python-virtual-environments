<h1>
  <span class="headline">Intro to Python Virtual Environments</span>
  <span class="subhead">Setup</span>
</h1>

## Setup

Open your Terminal application and navigate to your **`~/lessons`** directory:

```bash
cd ~/lessons
```

Make a new directory called **`pipenv-test`**, then enter this directory:

```
mkdir pipenv-test
cd pipenv-test
```

## Package Installation

You can install `pipenv` with Python package manager:

```sh
pip3 install pipenv
```

This will install the `pipenv` module globally, which is exactly what we want.

Use the following command to verify the installation.

```bash
pipenv --version
```

## **Adding Pipenv to PATH**

When you try to use `pipenv` to install dependencies the first time, you may see a warning that `pipenv` is installed but **not found in your terminal**, you need to add it to your system’s `PATH` variable. Follow the instructions based on your operating system:

### **For macOS (zsh)**

If you are using macOS and **Zsh** (the default shell on macOS Catalina and later), run:

```bash
echo 'export PATH="$HOME/Library/Python/3.9/bin:$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

> 🛠 **Note:** If you are using a different Python version (such as 3.10 or 3.11), update `3.9` in the path accordingly.

### **For Git Bash on Windows**

If you are using **Git Bash** on Windows, add Pipenv’s installation path to your `PATH` variable:

```bash
echo 'export PATH="$HOME/AppData/Roaming/Python/Python39/Scripts:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

> 🛠 **Note:** If your Python version is **not 3.9**, replace `Python39` with your correct version (such as `Python310` for Python 3.10).

### **For Linux (Ubuntu)**

On **Ubuntu (or any Linux system using Bash)**, run:

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

> 🛠 **Note:** This ensures user-installed Python packages (including Pipenv) are available system-wide.

### **Final Verification**

After applying the appropriate fix, restart your terminal and check if Pipenv is now accessible by running:

```bash
pipenv --version
```

If you see a version number, the setup is complete! 🎉

## Open project folder

Open the `pipenv-test` directory in VSCode:

```bash
code .
```
