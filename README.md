# Rapid7 Style Guide Linter
This repository contains the Rapid7 style guide linter. It checks for grammar and spelling rules for Rapid7 public facing communication. 

This can be added to your repository as an action or you can download the release and use it locally. 

This is for the Vale linter (https://github.com/errata-ai/vale) and Vale action (https://github.com/errata-ai/vale-action).

# Current Problems

The action currently accepts a path to a single folder or to all folders. It tries to lint every single file, which times out because of the
API limits. Using this locally, it isn't a problem because you can just point the tool at the file / files you are editing. If we want this to run on the repo, this needs to be solved. 


# Use as an action
1. Add a .vale.ini file to your local repository. See the example below. 
2. Create the GH action for Vale. 
3. Add the link for the linter release and ini file to your action. 

# Use locally
Install Vale https://errata-ai.gitbook.io/vale/

1. Add a vale.ini file at the top level of your directory.
2. Copy the folder ux-writing-r7-vale into your local .github folder. 
3. Then use one of the following commands to run vale
- `vale --glob='*.md' .`
- `vale filePath/fileName`

See https://github.com/tperry-r7/ux-writing-linter-test for an example of setup.

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