# installation
pip install -i https://test.pypi.org/simple/ anyNote2-MichaVardy


# Use
```
    $ anyNote init                  # initializes an anyNote repository in current working directory
    $ anyNote init -sd <dir>        # initializes an anyNote repository in directory specified directory
    $ anyNote SET_PATH              # set paths for different programs used for keywords
    $ anyNote SET_KEYWORD_TEMPLATE  # keyword template, all template files are stored in template dir in anyNote root, file name is keyword name
    $ anyNote SET_KEYWORD_OPTION    # sets keyword options, usually used to run to open external programs
    $ anyNote                       # traverse through hiarchy tree
    $ anyNote -pdf                  # output anyNote as pdf
    $ anyNote -rm <node>            # remove selected child branch
    $ anyNote WRITE                 # traverse through hiarchy tree, once the correct node is selected, insert text
    $ anyNote WRITE -g              # select global notes directory, should be set in set_path
    $ anyNote WRITE -d <dir>        # traverse through hiarchy tree, once the correct node is selected, insert text
    $ anyNote TODO                  # keyword node, saves todo information that can be displayed in a todo list
    $ anyNote TODO -l               # keyword node, todo list display
    $ anyNote STATUS                # keyword node, saves status information which can be displayed as status report list
    $ anyNote STATUS -l             # keyword node, status report list
    $ anyNote REFERENCES            # keyword node, saves links to documents and urls, 
    $ anyNote REFERENCES -url       # keyword node, opens all urls
    $ anyNote REFERENCES -pdf       # keyword node, opens all urls
    $ anyNote REFERENCES -all       # keyword node, opens all references, can only open if file type is given in SET_PATH
    $ anyNote SVG                   # keyword node, saves link to svg file, can be opened with svg editor
    $ anyNote SVG -pdf              # keyword node, opens all svg in node as pdf 
    $ anyNote TEST                  # saves pytest file, can be opened with ide
    $ anyNote TEST -run             # saves pytest file, runs test code
```
# Hiarchy tree
- anyNote hiarchy is stipulated in first header and deliniated using -
- a number of headnodes will pop up, and the user can start typing the headnode string which can be tab autocompleted
- as nodes are selected the selection pool will contain only children of last selected node
- the entire node path will be displayed next to the tree
- tabs can be used to auto-complete node string or to alternate between children in children display
- if a node is written that is not in the list of children, a new child will be added
```
# example: head-node
$anyNote tree subject1
    --> subject1
        subject2
        subject3
# example: node
$anyNote tree subject1 - sub-subject 2 - sub sub subject 3 - sub sub sub su
    --> sub sub sub subject 1
        sub sub sub subject 2
        sub sub sub subject 3
        ...
    ...
```


