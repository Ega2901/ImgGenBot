```markdown
# 📸 ImgGenBot (Tutorial)

## 🛠️ Part 1: Setup and Preparation

Before we start building the Telegram bot with the Flux model for image generation, we need to set up the development environment. This part of the tutorial will guide you through creating a Python virtual environment, installing `Poetry`, and adding the necessary packages for the project.

### 🧑‍💻 Step 1: Install Python 3.12

First, make sure you have Python 3.12 installed on your system. You can verify this by running the following command:

```bash
python3 --version
```

If Python 3.12 is not installed, download and install it from the official Python website [here](https://www.python.org/downloads/).

### 🧑‍💻 Step 2: Set Up a Virtual Environment

A virtual environment ensures that all dependencies and libraries are isolated within the project, avoiding conflicts with system-wide packages. Here's how to create one:

1. Navigate to your project directory (or create a new one):

   ```bash
   mkdir imggenbot
   cd imggenbot
   ```

2. Create a virtual environment:

   ```bash
   python3 -m venv venv
   ```

3. Activate the virtual environment:

   - On Linux/macOS:

     ```bash
     source venv/bin/activate
     ```

   - On Windows:

     ```bash
     .\venv\Scripts\activate
     ```

After activation, your terminal should show `(venv)` at the beginning of the prompt, indicating that the virtual environment is active.

### 🧑‍💻 Step 3: Install Poetry

[Poetry](https://python-poetry.org/) is a powerful tool for managing dependencies, packaging projects, and handling virtual environments in Python.

To install Poetry, run the following command (assuming you have Python 3.12 installed):

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

After installation, verify that Poetry is installed:

```bash
poetry --version
```

This should display the current version of Poetry.

### 🧑‍💻 Step 4: Initialize a New Project with Poetry

Now that Poetry is installed, you can initialize your project with it:

```bash
poetry init
```

Follow the prompts to configure the project:

- Package name: `imggenbot`
- Version: `0.1.0`
- Description: `A Telegram bot for generating images from text descriptions using the Flux model`
- Author: [Your Name]
- License: [Your License of Choice]

Poetry will create a `pyproject.toml` file, which is used to manage your project's dependencies.

Alternatively, you can skip this step and directly update your `pyproject.toml` file with the following configuration:

```toml
[tool.poetry]
name = "bot"
version = "0.1.0"
description = ""
authors = ["Ega2901 <mr.tuzharov@gmail.com>"]
readme = "README.md"

[tool.poetry.dependencies]
python = "^3.12"
aiogram = "^3.13.0"
huggingface-hub = "^0.24.7"
python-dotenv = "^1.0.1"
fastapi = "^0.103.0"
uvicorn = "^0.23.0"

[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"
```

### 🧑‍💻 Step 5: Add Required Packages

After setting up the `pyproject.toml`, install the necessary dependencies with Poetry. The updated dependencies include **Aiogram**, **Hugging Face Hub**, **dotenv**, **FastAPI**, and **Uvicorn**:

```bash
poetry install
```

This command will install the following dependencies:

- **Aiogram**: The framework for building the Telegram bot.
- **Hugging Face Hub**: To integrate the Flux model for text-to-image generation.
- **Python-dotenv**: For managing environment variables securely (for API keys and other sensitive data).
- **FastAPI**: The high-performance web framework for building APIs.
- **Uvicorn**: The ASGI server for running FastAPI applications.

Poetry will also install any additional dependencies required by these packages.

### 🧑‍💻 Step 6: Activate Poetry’s Virtual Environment

To activate the virtual environment Poetry manages, run the following command:

```bash
poetry shell
```

This will activate the environment, and you’ll see your prompt change to `(imggenbot-py3.12)`.

### 🧑‍💻 Step 7: Verify Installation

To verify everything was installed correctly, you can check the versions of the installed packages and tools:

```bash
python --version
poetry --version
uvicorn --version
```

You should see Python 3.12, the version of Poetry you installed earlier, and Uvicorn.

---

## 🎉 Congratulations!

You have successfully set up the environment for your **ImgGenBot** project, including the necessary dependencies like `aiogram`, `huggingface-hub`, `dotenv`, `fastapi`, and `uvicorn`. In the next part, we’ll start implementing the bot’s logic using **Aiogram** and building the API with **FastAPI**.
```


