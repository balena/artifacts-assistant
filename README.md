# Release Assistant

This is a pocket app that maintains a CHANGELOG.md file and a `dist` folder
containing binary artifacts that should be versioned.

Before running it, install the required dependencies with:

    $ ./assistant.py reqs > requirements.txt
    $ pip3 install --user -r requirements.txt

Then run:

    $ ./assistant.py

Point your browser to http://127.0.0.1:5757/ and enjoy!

P.S.: You may want to configure some settings in the `assistant.py` script,
such as the URL of your bugtracking system (see the variable
`BUGTRACKING_URL`).


## Working with branches

Put `assistant.py` on your project and create a file named `.branches.py`
containing a Python-like set with the branches used to store artifacts.

For example:

    {
      'branchA',
      'branchB'
    }

You may have other branches in the repository, but only these two will be
handled by the `assistant.py`.

When handling multiple branches, don't forget to replicate the `assistant.py`
script.


## The CHANGELOG.md file

You may edit the file manually for fixing past log entries. In this case,
please follow the format below:

    ## [version] - [date]
    [comments]

Avoid to use headings in the `[comments]` as they may conflict with the version
headers. Stick to normal paragraphs, lists, etc.
