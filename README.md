# NVIDIA-Modulus Environment Setup

A walkthrough for setting up the environment for NVIDIA-Modulus.

---

## 1. Create and Activate a Python Virtual Environment

### **Step 1: Create a Virtual Environment**
To create a virtual environment for NVIDIA-Modulus, navigate to your home directory or the directory where you manage virtual environments, and run:

```bash
python3 -m venv <your_virtualenv_name>
```

(optional) If you have an active Conda environment, deactivate it to avoid conflicts:

```bash
conda deactivate
```

### **Step 3: Activate the Virtual Environment**
Activate the newly created virtual environment:

```bash
source <your_virtualenv_name>/bin/activate
```

---

## 2. Install NVIDIA-Modulus
Ensure that the Modulus repository is located in the desired directory (preferably outside the virtual environment directory). To build NVIDIA-Modulus locally from source, follow these steps:

```bash
git clone git@github.com:NVIDIA/modulus.git && cd modulus
pip install --upgrade pip
pip install .
```

---

## 3. Install Required Packages

### **Step 1: Update `pip`**
Before installing the required packages, ensure that `pip` is up-to-date:

```bash
pip install --upgrade pip
```

### **Step 2: Install Dependencies**
Navigate to the base directory of this GitHub repository and install the required packages:

```bash
pip install -r requirements.txt
```

The `requirements.txt` file will handle all necessary package versions.

---


For additional assistance, feel free to contact the repository maintainers.
