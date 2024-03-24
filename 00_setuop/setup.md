# Setup Your Dev Environment

We have setup this repository and course with a _dev container_ that comes with a Python 3 runtime. Open the repo in GitHub Codespaces or on your local Docker Desktop, to activate the runtime automatically. Then open th Jupyter notebook and select the Python 3.x kernel to prepare the Notebook for execution.

## 1. Create `.env` file

To configure this, we need to setup local environment variables for Azure as follows:

1. Look in the root folder for a `.env.copy` file. It should contain a list of name-value pairs like this:

   ```bash
   OPENAI_API_KEY='<add your key here>'
   ```

   This should create an identical copy _except that this file is .gitignore-d and will never get checked into source control_. We can now populate **this .env file** with the environment variable values (secrets) without fear of them being checked in accidentally. You can now move to the next section to start populating these variables.

```bash
OPENAI_API_KEY='<add your OpenAI key here>'
```

## 2. Populate `.env` file

Let's take a quick look at the variable names to understand what they represent:

| Variable                           | Description                                                                        |
| :--------------------------------- | :--------------------------------------------------------------------------------- |
| OPENAI_API_KEY                     | This is the authorization key for using the service for non-Azure OpenAI endpoints |
| OPENAI_EMBEDDINGS_DEPLOYMENT       | This is the _text embeddings_ model deployment endpoint                            |
|                                    |                                                                                    |

For context, the last two variables refer to specific models that are used in chat completion (text generation model) and vector search (embeddings model) activities that are frequently used in generative AI applications. In the following sections, we'll locate the _values_ for these variables and set them in `.env` (replacing the content within the `' '`, but preserving the quotes).


**Don't forget to save the .env file when done**. You can now exit the file and return to the instructions for running the notebook.

### 2.3 Use OpenAI Public API

Your OpenAI API key can be found in your [OpenAI account](https://platform.openai.com/api-keys?WT.mc_id=academic-105485-koreyst). If you don't have one, you can sign up for an account and create an API key. Once you have the key, you can use it to populate the `OPENAI_API_KEY` variable in the `.env` file.
