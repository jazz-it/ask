# ask
ChatGPT in your terminal

The application accepts multiline inputs until the sentence ends with a questiton mark.
Editting multiline inputs is available by using cursor keys on your keyboard.

Before using this application, you should create a file `Config.py` in the same directory with
this script and put just the following content in it:

```
OPENAI_API_KEY = "YOUR_API_KEY_GOES_HERE"
```

Create your KEY here: https://beta.openai.com/account/api-keys

# Available keywords:
---
HELP   - displays help
ADD    - adds the previous answer to your bookmark
LIST   - displays your bookmark
CODE   - disables two empty lines to trigger submission
NOCODE - enables two empty lines to trigger submission (default)
EXIT   - same as any other input less than 7 characters long ends the application

Hitting ENTER after two empty lines in a NOCODE mode is a handy cross-platform equivalent 
for `[Ctrl+Z]`+`[ENTER]` in Windows, or `[Ctrl+D]` in Linux/Mac terminals. It basically 
terminates standard input by outputting EOF (end of file).
