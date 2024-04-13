# food_recsys_bot
A recsys for healthy recipes, integrated into a telegram chatbot and focused on persuasive explanations to encourage users to adopt healthier eating habits.

This is an enhanced version of the bot at this [repo](https://github.com/swapUniba/FoodRecSysBot), I have also pushed a .pdf file in which all the updates are listed.

[@food_recsys_bot](https://t.me/food_recsys_bot)

## Set Up
First and foremost, install the requirements with the command: `pip install -m requirements.txt`.
Check whether or not all the libraries have been installed, if any problem shows up, try installing the libraries without specifying any version.

The bot necessitates three servers that must be up and running to let it be fully operative:
- the bot itself -> `python FoodRecommenderSys.py`
- the recommendation module -> `python food_rs_webservice.py`
- the explanation module -> `python web_expl.py`
Their names are quite self-explanatory on what they do or handle.

The bot is built on the [python-telegram-bot library v20.7](https://pypi.org/project/python-telegram-bot/20.7/)  and it won't run if the credentials are not set up correctly:
- bot's APIs token: `6795730001:AAG-srtuPSbU3DeJzGgQQv8app0ERztqr6U`
- you will also need a new Google Service Account to generate credentials specifically for the Python connection between Dialogflow and the bot. Once you have linked the Service account to DialogFlow you will need to generate the JSON file, import it into your workspace and the link it in the main module of the bot itself (FoodRecommenderSys.py)

You won't need a new DialgFlow agent, since I've pushed into this repository a .zip file that contains the entire agent.
Just import from the .zip it into your DialogFlow console. 



## Usage
About the actual use of the bot: \
Once you have it up and running, you can create your profile with the command `/create`. \
Follow the instructions, and at the end, if you want to see or modify your profile you can do it with the command `/modify`. \
Whenever you are satisfied with your profile, you can ask it for a suggestion [_all the words and sentences that trigger an intent are defined in the DialogFlow agent_]. \

The bot will give you the most appropriate recipe, but if you are not satisfied with the recipe, you can change it up to two times. \

From here you have three possibilities:
1. You can ask for more information about some aspects of the recipe (such as macros, cost, popularity, health benefits, sustainability, and so on...)
2. You can ask for a second (or third) suggestion, which will enable the option to ask for a comparison between the latest two recipes recommended. Now you can ask to compare them according to some criteria.
3. You can ask for a specific ingredient-based recipe (or you can specify a type of dish)
