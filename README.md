# Get Started

## Requirement:
* MkDocs:

** Get it in https://www.mkdocs.org/

** Follow the instructions in: 
http://opendata.atlas.cern/new/tutorials/hackathon-2019/document/

**For Latex-kind and Maths**

* python-markdown-math
Get it (install using pip) as mentioned in: https://github.com/mitya57/python-markdown-math

Once you get those installed:

You can follow this instruction:
``` shell
git https://github.com/LA-CoNGA-MiLab-RedClara/class-material-mkdocs.git
cd class-material-mkdocs 
mkdocs serve
```

To put it in App, you need to generate HTML by:
```
mkdocs build
```


Base coming from the work of our summer students
https://github.com/artfisica/ATLASOpenDataGuide

and previous 8 TeV release
https://github.com/artfisica/documentation-8tev-atlas-open-data


---
# Building your project documentation

[**MkDocs**](https://www.mkdocs.org) is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation.
Documentation source files are written in **Markdown**, and configured with a single YAML configuration file.

## **Mkdocs installation**

* **Prerequisite: Python and Pip**

In order to manually install MkDocs you'll need Python installed on your system, as well as the Python package manager, pip. You can check if you have these already installed from the command line:

**On Windows:**

```
C:\Users\User>python --version
Python 3.5.4
C:\Users\User>pip --version
pip 9.0.1
```

**On MacOS or Linux**

```
$ python --version
Python 2.7.2
$ pip --version
pip 1.5.2
```

* **Installing Python**

Install [Python](https://www.python.org/) by downloading an installer appropriate for your system from [python.org](https://www.python.org/downloads/) and running it.

**Note:**
If you are installing Python on Windows, be sure to check the box to have Python added to your PATH if the installer offers such an option (it's normally off by default).

![path](https://www.mkdocs.org/img/win-py-install.png)

* **Installing Pip**

If you're using a recent version of Python, the Python package manager, pip, is most likely installed by default. However, you may need to upgrade pip to the lasted version:
`pip install --upgrade pip`

If you need to install pip for the first time, download get-pip.py. Then run the following command to install it:
`python get-pip.py`

* **Installing MkDocs**

Install the `mkdocs` package using pip:
```
pip install mkdocs
```

You should now have the `mkdocs` command installed on your system. Run `mkdocs--version` to check whether successfully installed.

**On Windows:**
```
C:\Users\User>mkdocs --version
mkdocs, version 1.0.4
```
**On MacOS or Linux**
```
$ mkdocs --version
mkdocs, version 0.15.3
```
## **Getting started to edit**

* Clone this documentation to your device by git

Clone with ssh:
```
git clone ssh://git@gitlab.cern.ch:7999/atlas-outreach-data-tools/hackathon-docs.git
```
Clone with https:
```
git clone https://gitlab.cern.ch/atlas-outreach-data-tools/hackathon-docs.git
```

In your `hackathon-docs` folder, you will see a configuration file named `mkdocs.yml`, and a folder named `docs` that will contain your documentation source files.

![folder1](https://github.com/veritasalice/MarkdownPhotos/blob/master/folder1.png?raw=true)

Right now the `docs` folder just contains all the documentation pages, such as  `index.md`, `datasets.md` and the folders where the pages are saved.

![folder2](https://github.com/veritasalice/MarkdownPhotos/blob/master/folder2.png?raw=true)


MkDocs comes with a built-in dev-server that lets you preview your documentation as you work on it. Make sure you're in the same directory as the `mkdocs.yml` configuration file, and then start the server by running the `mkdocs serve` command:
```
C:\Users\User\hackathon\hackathon-docs>mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 190705 15:13:53 server:296] Serving on http://127.0.0.1:8000
[I 190705 15:13:53 handlers:62] Start watching changes
[I 190705 15:13:53 handlers:64] Start detecting changes
```

Open up `http://127.0.0.1:8000/` in your browser, and you'll see the pages you cloned being displayed:

![pic3](https://github.com/veritasalice/MarkdownPhotos/blob/master/yourDoc3.png?raw=true)

Use the editor you like to edit the files in `docs` and your changes will be displayed when saving them.



## **Using the Git to commit your changes**

By far, the most widely used modern version control system in the world today is Git.
In Git, every developer's working copy of the code is also a repository that can contain the full history of all changes.

**Prerequisites:**

* [Download](https://git-scm.com/downloads) and install Git
* [Apply for a Gitlab account](https://gitlab.cern.ch/)

**The working flow of Git:**

* Initialize your repository with `git init[directory]`
* Clone a repository onto your local machine with `git clone [URL]`
* Edit the docs using Mkdocs
* Stage all changes for the next conmmit with `git add [directory]`
* Commit the staged snapshot with `git commit -m ["commit message"]`
* If others have modified it, you can **check the updates** with `git fetch` and **update the resource** with `git pull`.
* Show unstaged changes between your index and working directory with `git diff`
* Review your changes before submitting with `git status`
* Push your changes to the remote Gitlab repository with `git push`

![gitFlow](https://i.stack.imgur.com/ODFYa.png)


Reference to [git cheet sheet](file:///C:/Users/User/Downloads/atlassian-git-cheatsheet.pdf) for details


