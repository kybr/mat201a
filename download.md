---
layout: page
title: Download
permalink: /download/
---

The Jupyter Notebooks for this course are currently hosted on Github: [201A-ipython](https://github.com/kybr/201A-ipython). Use `git` to clone the course repo like this:

	git clone --depth 1 https://github.com/kybr/201A-ipython

<!-- Or, if you prefer, download a .zip file [here](https://github.com/kybr/201A-ipython/archive/master.zip). -->

As the course progresses, we will update this repository. If you would like to get our updates, you have a couple options. **Note that both of these methods throw away any/all changes you made to notebooks in `201A-ipython`.** It is up to you to manually copy any work you want to keep. Jupyter offers a browser-based file/folder organizer that you may use to save your changed version of the course notebook. Here are the options:

1. Delete your current (now obsolete) copy of `201A-ipython` and clone `201A-ipython` again with the command above.
2. Clean and update your current repo using these commands:

```bash
cd path/to/201A-ipython
git reset --hard
git pull
```

If anything seems to break and you want some help, copy and paste your terminal session into a gist (https://gist.github.com) and email me the URL of that gist along with your question.
