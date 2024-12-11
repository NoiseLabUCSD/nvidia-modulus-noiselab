# NVIDIA-Modulus-Noiselab  
A guide to setting up the environment for NVIDIA-Modulus in the Noiselab Kraken environment.

---

## 1. Create and Activate a Python Virtual Environment  
To create a virtual environment for NVIDIA-Modulus in Kraken environemtn, follow these steps:

### **Step 1: Create a Virtual Environment**  
In your home directory or the directory where you manage virtual environments, run:  
```bash
python3 -m venv <your_virtualenv_name>
```

Ensure that the Python version in your virtual environment is **Python 3.10**.  
- The default Python version in Kraken is 3.10.  
- If you are using a Conda environment, it might default to a different version.  
  To avoid conflicts, deactivate the Conda environment using:  
  ```bash
  conda deactivate
  ```

### **Step 2: Activate the Virtual Environment**  
Activate your newly created virtual environment:  
```bash
source <your_virtualenv_name>/bin/activate
```

---

## 2. Install Required Packages  
Once your virtual environment is activated, navigate to the base directory of this GitHub repository. Then, install the required packages, including `nvidia-modulus` and `nvidia-modulus-sym`:  
```bash
pip install -r requirements.txt
```

---

### **Important Notes:**  
1. **PyTorch Version Compatibility:**  
   Ensure that the version of PyTorch installed is compatible with **CUDA 12.1**, not CUDA 12.5.  
   - The default CUDA version in Kraken is **12.5**, but the `requirements.txt` file will ensure the correct version of PyTorch is installed.  

2. **Verify Installation:**  
   After the installation, you can verify that the correct PyTorch version is being used:  
   ```bash
   python -c "import torch; print(torch.version.cuda)"
   ```

---

## Summary  
This guide helps you set up an isolated Python environment for NVIDIA-Modulus in Kraken. By following the steps, you ensure compatibility and avoid conflicts with the default system configurations.

For additional support or questions, feel free to reach out to the repository maintainers.