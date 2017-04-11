---
layout: page
title: Download
permalink: /download/
---

The materials for this class (e.g., syllabus, notebooks, assignments) are hosted on Github: [mat201a](https://github.com/kybr/mat201a). Use `git` to clone the course repo like this:

	git clone --depth 1 https://github.com/kybr/mat201a

These materials are used to generate the course website found here: [http://www.mat.ucsb.edu/201A](http://www.mat.ucsb.edu/201A)

<!-- Or, if you prefer, download a .zip file [here](https://github.com/kybr/201A-ipython/archive/master.zip). -->

As the course progresses, we will update the course repository and website. If you would like to get our updates, you have a few options:

1. Browse or download notebooks from the course website (see [notebooks]({{ site.url | append:site.baseurl}}/notebook)).
2. Get a _fresh_ clone the course repository like this:

	git clone --depth 1 https://github.com/kybr/mat201a

3. Pull inside an existing clone like this:

```bash
cd path/to/mat201a
git reset --hard # this throws away all your changes!!!
git pull
```

Note that if you use the git method, you will need to install [git lfs](https://git-lfs.github.com) beforehand.

If anything seems to break and you want some help, copy and paste your terminal session into a gist (https://gist.github.com) and email me the URL of that gist along with your question.
