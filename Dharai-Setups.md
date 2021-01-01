#GPT3 Installation and Setups

1) Clone the repo https://github.com/dharai/gpt3-sandbox

2) Create a file openai.cfg and add the API key provided by Open AI

File content:
OPENAI_KEY='Your key goes here'

3) Save the openai.cfg file in the root directory of above cloned repo (Root here would be gpt3-sandbox folder)
From command line, run

export OPENAI_CONFIG=/Path to gpt3-sandbox/openai.cfg

4) Setup Virtual Environment in gpt3-sandbox root folder

  python -m venv your_env_name

  source your_env_name/bin/activate

5) Install libraries as listed in the requirements.txt file

   pip install -r api/requirements.txt

6) Install yarn

   yarn install

   yarn upgrade

   yarn

   yarn run start (This will check and run react-scripts)

   Exit the react-scripts (Press Control + C)

   Note: if you run into errors while executing the example scripts for OpenAI, check this document and correct the errors accordingly
   https://stackoverflow.com/questions/47612580/react-scripts-command-not-found

7) Check if the Open AI connection is successful by executing sample scripts

   > python

   >>> from api import GPT, Example, set_openai_key
   >>> gpt = GPT()
   >>> set_openai_key(key)
   >>> prompt = "integral from a to b of f of x"
   >>> print(gpt.get_top_reply(prompt))
   output: integral from at to be of f of x

8) Validate OpenAI with some examples

   run the receipes example

   python examples/run_recipe_app.py

   Browser would open (Google Chrome would open)

   UI would have a Text box to enter the question. Click submit and check the results.

   To close this example window, click Control and C in the atom shell.

9) Run other examples

   python examples/run_command_to_email_app.py

   python examples/run_analogies_app.py
