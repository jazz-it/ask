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
* SAVE   - saves the entire bookmark to `output.txt`
* EXIT   - same as any other input less than 7 characters long ends the application

> Hitting ENTER after **two empty lines** in a `NOCODE` mode is a handy \
> cross-platform equivalent for `Ctrl+Z`+`ENTER` in Windows, or `Ctrl+D` in Linux/Mac terminals.\
> It basically terminates standard input by outputting EOF (end of file).

The biggest advantage of using this application is speed, as opposed to the original web interface. Also, whilst using this application you can combine several answers into one larger text using the `add` keyword. After you finish your research work, list all the saved parts added to bookmark by using `list`. Given that this bookmark mode of operation is dependent to each separate session, the application makes sure that you don't accidentally exit the program if you haven't display your bookmark or store it yet.

> The bookmark could be stored to an external file, so your research could be saved even after each session expires.

Unlike some other scripts, this one allows you to enter more than just one line in your question, it simplifies the input so that it is enough to press ENTER 2x to trigger the question submission, which can be turned off in the special `CODE` mode.

> Be aware that using ChatGPT via API does not offer any possibility of contextual conversation, \
> i.e. previous answers have no contextual significance in the current question, so you may want to use \
> the conversation history with the help of the up/down cursor keys more often.
