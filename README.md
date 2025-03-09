# Parlant Tutorial

This project is a Python-based environment setup using **Poetry** for dependency management.  
It includes a structured **package setup** inside a `base/` directory.

---

## **🚀 Project Setup Guide**

### **1️⃣ Create a New Project Directory**
Run the following commands to create a project folder and navigate into it:
```sh
mkdir parlant-tutorial
cd parlant-tutorial
```

---

### **2️⃣ Initialize Poetry**
Initialize a new Poetry project:
```sh
poetry init
```
During this step, provide:
- **Project Name** (e.g., `parlant-tutorial`)
- **Version** (e.g., `0.1.0`)
- **Description** (Optional)
- **Author Name & Email**
- **License** (Optional)
- **Python Version** (e.g., `>=3.10`)
- **Dependencies** (Press Enter to skip for now)

---

### **3️⃣ Configure Poetry to Recognize the Project Structure**
Modify `pyproject.toml` to **specify the package directory**:
```toml
[tool.poetry]
packages = [{ include = "base" }]
```

---

### **4️⃣ Install Dependencies Without Installing the Project**
Since we are using the project as a directory (not a library), install dependencies without installing the project as a package:
```sh
poetry install --no-root
```

---

### **5️⃣ Create the Project Directory Structure**
Create the `base/` directory:
```sh
mkdir base
```
Then, create the required Python files:
```sh
touch base/__init__.py
touch base/main.py
```

---

### **6️⃣ Create a Virtual Environment Inside the Project**
By default, Poetry creates a virtual environment **outside** the project.  
To keep it inside, create a local `.venv/`:
```sh
python3 -m venv .venv
```
Check if the `.venv/` directory exists:
```sh
ls -la
```

---

### **7️⃣ Activate the Virtual Environment**
Activate the venv so you can use Python and Poetry inside it:

#### **For macOS/Linux:**
```sh
source .venv/bin/activate
```

#### **For Windows (PowerShell):**
```powershell
& .venv\Scripts\activate
```

---

### **8️⃣ Install Dependencies**
Once the virtual environment is activated, install all dependencies:
```sh
poetry install
```

---

## **📂 Project Structure**
After completing the setup, your project should look like this:
```
parlant-tutorial/
│── .venv/              # Virtual environment (inside project)
│── base/               # Main package
│   ├── __init__.py
│   ├── main.py
│── pyproject.toml      # Poetry configuration file
│── poetry.lock         # Dependency lock file
│── README.md           # Project documentation (this file)
```

---

## **🎯 Running the Project**
To run your project, activate the virtual environment first:
```sh
source .venv/bin/activate  # (macOS/Linux)
```
Then, execute the main script:
```sh
python base/main.py
```

---

## **❌ Uninstall or Remove the Virtual Environment**
If you want to **remove the venv**, run:
```sh
poetry env remove python
```

To recreate the environment:
```sh
poetry install
```

---

## **📌 Notes**
- Always activate the virtual environment before running any Python scripts.
- Use `poetry add <package>` to install new dependencies.
- Use `poetry remove <package>` to uninstall dependencies.

---

## **🤝 Contributing**
Feel free to fork the repo and submit a pull request!

---

## **📜 License**
This project is licensed under the MIT License.

---

🚀 **Now your Parlant tutorial project is fully set up and ready to go!**  
```

---

### **🔥 Why This README?**
- It provides a **step-by-step guide** for setting up the project.
- It includes **important commands** for Poetry and virtual environment management.
- It **documents** the project structure and **how to run** it.

This README should serve as a **quick reference** for anyone using your project! 🚀 Let me know if you'd like to add more details!
