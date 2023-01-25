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


![ask](https://user-images.githubusercontent.com/411471/214698622-62921907-e3ed-40f0-8af1-0b566c0bce09.gif)


## Available keywords:

* HELP   - displays help
* ADD    - adds the previous answer to your bookmark
* LIST   - displays your bookmark
* CODE   - disables two empty lines to trigger submission
* NOCODE - enables two empty lines to trigger submission (default)
* EXIT   - same as any other input less than 7 characters long ends the application

Hitting ENTER after **two empty lines** in a NOCODE mode is a handy cross-platform equivalent 
for `Ctrl+Z`+`ENTER` in Windows, or `Ctrl+D` in Linux/Mac terminals. It basically 
terminates standard input by outputting EOF (end of file).

The biggest advantage of using this application is speed, as opposed to the original web interface. Also, whilst using this application you can combine several answers into one larger text using the `add` keyword. After you finish your research work, list all the saved parts added to bookmark by using `list`. Given that this bookmark mode is strictly dependent to each separate session, the application makes sure that you don't accidentally exit the program if you haven't executed the `list` command prior to exiting, but only in case you already have some content saved in the bookmark and haven't seen it yet. Unlike some other scripts, this one allows you to enter more than just one line in your question, it simplifies the input so that it is enough to press ENTER 2x to trigger the question submission, which can be turned off in the special `CODE` mode. Each line can be edited separately before sending using the cursor keys while asking a question.

It is important to be aware that ChatGPT via API mode does not offer the possibility of contextual conversation, i.e. previous answers have no contextual significance in the current question, so you may want to use the conversation history with the help of the up/down cursor keys more often.
