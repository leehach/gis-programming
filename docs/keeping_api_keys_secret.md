# Keeping API Keys Secret

In data science workflows you will often retrieve data or engage in online geoprocessing using API keys. These keys should not appear in your bare code, where they could be copied and used by someone you share your code with, and should *never* be committed to a GitHub repo, for the same reason (it is essentially highly public code sharing) as well as the fact that once the key is in the repo it could always be recovered from the history even if you delete it. In fact, there are bots that crawl GitHub looking for keys that developers have committed and will copy them almost as soon as they are posted.

The solution is to store the key in a separate file (which I will not demonstrate) or an environment variable, and then read the key from the file or environment variable in your Python code.

## Adding a Key to a Conda Environment

Since we are working in conda environments in this class, the best way to do this is to add the key to the conda environment variables, rather than to the operating system environment variables. This also makes it possible to use different keys for different project, which may be required in order to keep track of what usage gets charged to which project.

In order to add the environment variable to a system with Anaconda/Miniconda, run the following terminal command:

```sh
conda env config vars set VAR_NAME=var_value -n environment-name
conda activate environment-name
```

Note that if the environment is already activated, you do not need to specify the environment name with `-n environment-name`. You *do* need to reactivate the environment if you need access to the key in the current terminal session, or just close the terminal if you will use it elsewhere.

Stored environment variables can be checked with:

```sh
conda env config vars list
```

An environment variable can be deleted with:

```sh
conda env config vars unset VAR_1 VAR_2 VAR_3 ...
```

## Accessing an Environment Variable in Python

In Python, when you need access to the API key, you need to read it in from the environment variable. This is incredibly easy:

```python
import os

api_key = os.environ["VAR_NAME"]
```

Then use the `api_key` in any API call that needs it.
