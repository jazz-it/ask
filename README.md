# ask
ChatGPT in your terminal

The application accepts multiline inputs until the sentence ends with a questiton mark.
Editting multiline inputs is available by using cursor keys on your keyboard.

Before using this application, you should create a file `config.py` in the same directory with
this script and put just the following content in it:

```
OPENAI_API_KEY = "YOUR_API_KEY_GOES_HERE"
```

Create your KEY here: https://beta.openai.com/account/api-keys


![ask-3](https://user-images.githubusercontent.com/411471/214931191-6573e952-9a2f-41a7-a681-3d2b0542e8ec.gif)


## Available keywords:
* HELP   - displays help
* ADD    - adds the previous answer to your bookmark
* LIST   - displays your bookmark
* NOTE   - adds a custom text to your bookmark
* CODE   - disables two empty lines to trigger submission
* NOCODE - enables two empty lines to trigger submission (default)
* LVLn   - adjusts the level of creativity, `n` should be any integer [0-5]
* SAVE   - saves an entire bookmark to `output.txt`
* EXIT   - same as any other input less than 7 characters long - ends the application

> Hitting ENTER after **two empty lines** in a `NOCODE` mode is a handy \
> cross-platform equivalent for `Ctrl+Z`+`ENTER` in Windows, or `Ctrl+D` in Linux/Mac terminals.\
> It basically terminates standard input by outputting EOF (end of file).

## LVL
The "level of creativity" is actually the temperature argument for GPT-3, where  creativity of 5 means the temperature of 1. If you set the creativity value to 0 you will get no randomness. GPT-3 will always produce the same output for a given quesiton. On the other hand, setting the creativity value to 5 will deliver very inconsistent and sometimes interesting results. Even for open-ended tasks you should use a temperature value of 5 only in special situations. It is more common for story completion or idea generation to see temperature values between 4 and 5.
The default creativity value is 2 (which equals temperature of 0.4) and the creativity power bar is displayed within the prompt.

## Advantages:
The biggest advantage of using this application is speed, as opposed to the original web interface. Also, whilst using this application you can combine several answers into one larger text using the `add` keyword. After you finish your research work, list all the saved parts added to bookmark by using `list`. Given that this bookmark mode of operation is dependent to each separate session, the application makes sure that you don't accidentally exit the program if you haven't display your bookmark or store it yet.

> The bookmark could be stored into an external file, \
> so your research could be saved even after each session expires.

Unlike some other scripts, this one allows you to enter more than just one line in your question, it simplifies the input so that it is enough to create two empty lines to trigger the question submission, which can be turned off in the special `CODE` mode.

> Be aware that using ChatGPT via API does not offer any possibility of contextual conversation, \
> i.e. previous answers have no contextual significance in the current question, so you may want to use \
> the conversation history with the help of the up/down cursor keys more often.


## Output:
Here's an example of a generated `output.txt`:


<code>
Alert, Nunavut, Canada.

^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^
I need to come up with a nice title here.
----------------8<-------------[ cut here ]------------------



Alert, Nunavut, Canada is an amazing place with a unique history and culture. Located in the northernmost part of the country, Alert is the northernmost permanently inhabited place in the world. This remote community is home to a population of just over five hundred people, and is the northernmost settlement on the planet.

Alert is a fascinating place with a unique history. It was founded in 1950 as a weather station and has since served as a research station for the Canadian government. It is now the home of the Canadian Forces Station Alert, a military base that is used for surveillance and communication purposes. Despite its remote location, Alert is connected to the rest of the world through satellite communications.

The culture of Alert is also unique. The population is comprised of Inuit, Cree, and Dene people. The Inuit are the original inhabitants of the area, and their culture is still very much alive in the community. The Inuit have a deep connection to the land, and their culture is reflected in the traditional clothing, food, and language of the community.

Alert is also home to some amazing wildlife. The area is home to polar bears, Arctic foxes, caribou, and many other species of animals. The Arctic is also home to a variety of birds, including snow geese, loons, and ptarmigans. The area is also home to a wide variety of fish, including Arctic char, cod, and salmon.

Alert is an amazing place with a unique history and culture. Despite its remote location, the community is connected to the rest of the world through satellite communications. The culture of the community is reflective of the Inuit, Cree, and Dene people who call it home. The area is also home to a variety of wildlife, and is a great place for wildlife watching.

Alert is a place of beauty and wonder. It is a reminder of the importance of preserving the environment and respecting the

There are approximately 20 towns in the world with more than 1 million people that were founded within the last 100 years.

^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^v^
Reminder: find out more about those cities.
----------------8<-------------[ cut here ]------------------



▲▲▲ Generated on 26.01.2023 18:52:09 ▲▲▲</code>
