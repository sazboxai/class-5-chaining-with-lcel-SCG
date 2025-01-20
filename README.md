# Class 5: Chaining with LCEL

## Introduction
In this class, we will discuss chaining and introduce the [LangChain Expression Language (LCEL)](https://python.langchain.com/docs/concepts/lcel/), a declarative way to easily compose chains together.

## Slides
[Slides](https://docs.google.com/presentation/d/1M5pQT-OCFYugkZ2Hs6dt9xj0SU0ZWX1aVonYh2JfPsM/edit?usp=sharing)

## Prerequisites
Before you begin, ensure you have met the following requirements:
- Docker (recommended)
- Python 3.11.0 or greater (virtual environment setup)

### Set up environment variables:
- Copy the sample environment file:
  ```
  cp .env.sample .env
  ```
- Edit the `.env` file and add your API keys and other required variables:
  ```
  OPENAI_API_KEY=<your_openai_api_key>
  LANGCHAIN_API_KEY=<your_langchain_api_key>
  LANGCHAIN_TRACING_V2=true
  LANGCHAIN_PROJECT=week_4_1
  ```
## Docker

1. Start Jupyter to run the files with a local notebook:
   ```
   docker compose up jupyter
   ```
2. You may also run any new `.py` file you create in the root directory:
   ```
   docker compose run --rm main python <your_new_py_file>
   ```
Note: The Docker setup will automatically use the environment variables from your `.env` file.

## Running Different Scripts
You can use the provided `run.sh` script for easier execution.
Make sure to make the script executable with `chmod +x run.sh` in the CLI before using:
```
./run.sh jupyter
./run.sh <your_new_py_file>
```
## Local Setup (Alternative to Docker)
If you prefer to run the examples locally:

1. Ensure you have Python 3.11.0 or higher installed.
2. Clone the repository:
    ```
    git clone [repository-url]
    cd [repository-name]
    ```
3. Set up the virtual environment:
    ```
    python3 -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    pip install -r requirements.txt
    ```
4. Configure environment variables as described in the Setup section.
5. Export your `.env` variables to the system (python-dotenv should handle this for you in the main `.ipynb` file, but this is included for reference):
   **Linux / Mac / Bash**
      ```
      export $(grep -v '^#' .env | xargs)
      ```

5. Run the scripts:
    ```
    run the .ipynb files in VSCode (it will prompt you to allow the installation of ipykernel: do so) or another IDE that supports Jupyter Notebooks
    ```

## Need Help?
Reach out to the learning assistants in the Slack channel for this course