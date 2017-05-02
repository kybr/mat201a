---
layout: page
title: Homework
permalink: /homework/
---

<style>
table { border-collapse: collapse; }
table, th, td { border: 1px solid black; }
th, td { padding: 15px; text-align: left; }
</style>

Unless we say otherwise, **all assignments are due by 0600** (6AM) of the posted due date.

## General Homework Information

Homeworks are graded on a scale of 1 - 5. Keep in mind that grades will only be based on the nbviewer link you send via email, so make sure you proofread the nbviewer output to make sure everything rendered properly (including plots and embedded audio players / images).

Homework submissions will be published on the course website so that students can learn from one another throughout the course. Do not include any information you do not wish others to see (for example, perm numbers). Note that while modifying other people’s code for your own purposes is often acceptable (with proper attribution), plagiarism will not be tolerated.


## Assignment Rubric

-	1 point for meeting iPython notebook formatting requirements
-	1 point for meeting homework submission and email formatting requirements
-	1 point for meeting all the goals laid out in the assignment description
-	1 - 2 points for effort and execution 


## iPython Notebook Formatting Requirements

Failure to meet any of the following requirements will result in a one-point (20%) reduction of your homework grade:

-	The first cell in your iPython notebook must include the following text:
```python
# MAT 201A Spring 2017
# HW x
# FirstName LastName
# your.email@something.com
# Description of the work and/or important information
```
-	You must provide written descriptions to document your code throughout your notebook, including a high level explanation of your approach. Use markdown cells or inline comments to do so.
-	When working with images, each image must be displayed inline in your notebook. Use the `imshow` function.
-	When working with audio, each sound must be displayed (aka played) inline in your notebook. Use the `IPython.display.Audio` function.
-	When plotting data, always indicate what the plot is showing and what the axes represent. The `title`, `xlabel`, and `ylabel` functions are useful for this, but you can also provide this information in the form of markdown or inline comments.


## Email Formatting Requirements

You must submit your assignments as nbviewer URLs via email. Do not submit `.ipynb` or any other files as file attachments, they will not be graded. All code, plots, images, and audio should be embedded in your notebook. Failure to meet any of the following requirements will result in a one-point (20%) reduction of your homework grade:

- Message should be addressed to both the TA and the instructor
- Subject line should contain the following text `MAT 201A HW x FirstName LastName`
- Message body should contain a valid URL linking to your notebook on nbviewer.ipython.org


## Submission Procedure

Because certain notebook output (such as the embedded audio player) only renders properly in nbviewer, nbviewer URLs are REQUIRED. Follow ALL of the following directions when submitting your assignments. Failure to meet any of the following requirements will result in a one-point (20%) reduction of your homework grade:

### Make sure all the cells in your notebook ran properly and save the file:

![]({{ site.url | append:site.baseurl}}/image/00.png)
![]({{ site.url | append:site.baseurl}}/image/00a.png)

### Now use the text editor of your choice to open the notebook:

![]({{ site.url | append:site.baseurl}}/image/01b.png)

### Maybe you like TextEdit...

![]({{ site.url | append:site.baseurl}}/image/01.png)

### Select all the text in the file and copy it to the clipboard:

![]({{ site.url | append:site.baseurl}}/image/02.png)

### Head to [gist.github.com](https://gist.github.com). You'll see a blank template for creating a new Gist: 

![]({{ site.url | append:site.baseurl}}/image/03.png)

### Paste the contents of your file into the main text box:

![]({{ site.url | append:site.baseurl}}/image/04.png)

### Provide a useful filename for the Gist, and don't forget to include the extension '.ipynb':

![]({{ site.url | append:site.baseurl}}/image/05a.png)

### Click 'Create secret gist' (public is fine too) and Github will display your notebook:

![]({{ site.url | append:site.baseurl}}/image/05.png)

### Github will render the notebook to look like this:

![]({{ site.url | append:site.baseurl}}/image/06.png)

### Now click where it says 'Embed' and select 'Share' from the dropdown menu:

![]({{ site.url | append:site.baseurl}}/image/07.png)

### Select the URL text and copy, or use the 'Copy to clipboard' button:

![]({{ site.url | append:site.baseurl}}/image/08.png)

### Open a new tab and go to [nbviewer.jupyter.org](http://nbviewer.jupyter.org). Paste the URL you copied in the previous step into the main text box:

![]({{ site.url | append:site.baseurl}}/image/09.png)

### Click 'Go!':

![]({{ site.url | append:site.baseurl}}/image/10.png)

...and nbviewer will render your notebook:

![]({{ site.url | append:site.baseurl}}/image/11.png)


### ALWAYS proofread nbviewer’s rendering of your notebook. Once you’re sure that everything rendered properly, simply copy the current URL of this browser window

![]({{ site.url | append:site.baseurl}}/image/12.png)

### Finally, paste the URL into the body of your assignment submission email. Remember to include the TA as well as the instructor and format the subject line correctly:

![]({{ site.url | append:site.baseurl}}/image/99.png)

