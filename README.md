# Rapid7 Style Guide Linter
This repository contains the Rapid7 style guide linter. It checks for grammar and spelling rules for Rapid7 public facing communication. 

This can be added to your repository as an action or you can download the release and use it locally. 

This is based on

# Use as an action
1. Add a .vale.ini file to your local repository. See the example below. 
2. In GitHub click on the release tab. 
3. Grab the URL for the latest release by right clicking and copying the URL. 

# Use locally

# .vale.ini example


```
# This goes in a file named either `.vale.ini` or `_vale.ini`.
StylesPath = .github
MinAlertLevel = suggestion # suggestion, warning or error

# Only Markdown and .txt files; change to whatever you're using.
[*.{md,txt}]
# List of styles to load. Loading our styles from .github/valeStyles
BasedOnStyles = valeStyles
```