# Project Description

## Project Introduction

### Finding Lane Lines in a Video Stream

[Project Instruction](https://youtu.be/LatP7XUPgIE)

#### Project Instructions
To get started on the project, download or `git clone` [the project repository on GitHub](https://github.com/udacity/CarND-LaneLines-P1). You'll find the instructions in the README file. Click "Next" below to view information about setting up the project on your computer.

## Starter Kit Installation
In this term, you'll use Python 3 for programming quizzes, labs, and projects. The following will guide you through setting up the programming environment on your local machine.

There are two ways to get up and running:
1. Anaconda
2. Docker

We recommend you first try setting up your environment with Anaconda. It's faster to get up and running and has fewer moving parts.

If the Anaconda installation gives you trouble, try Docker instead.

Follow the instructions in [this README](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md).

Here is a great link for learning more about [Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111)

## Run Some Code!
Now that everything is installed, let's make sure it's working!

1. Clone and navigate to the starter kit test repository.
```bash
# NOTE: This is DIFFERENT from  https://github.com/udacity/CarND-Term1-Starter-Kit.git
git clone https://github.com/udacity/CarND-Term1-Starter-Kit-Test.git
cd CarND-Term1-Starter-Kit-Test
```
2. Launch the Jupyter notebook with Anaconda or Docker. **This notebook is simply to make sure the installed packages are working properly.** The instructions for the first project are on the next page.
```bash
# Anaconda
source activate carnd-term1 # If currently deactivated, i.e. start of a new terminal session
jupyter notebook test.ipynb
```
```bash
# Docker
docker run -it --rm -p 8888:8888 -v ${pwd}:/src udacity/carnd-term1-starter-kit test.ipynb
# OR
docker run -it --rm -p 8888:8888 -v `pwd`:/src udacity/carnd-term1-starter-kit test.ipynb
```
3. Go to http://localhost:8888/notebooks/test.ipynb in your browser and run all the cells. Everything should execute without error.

### Troubleshooting
#### ffmpeg
**NOTE**: If you don't have `ffmpeg` installed on your computer you'll have to install it for `moviepy` to work. If this is the case you'll be prompted by an error in the notebook. You can easily install `ffmpeg` by running the following in a code cell in the notebook.

```python
import imageio
imageio.plugins.ffmpeg.download()
```

Once it's installed, `moviepy` should work.

#### Docker
To get the latest version of the [docker image](https://hub.docker.com/r/udacity/carnd-term1-starter-kit/), you may need to run:
```bash
docker pull udacity/carnd-term1-starter-kit
```

Warning! The image is ~2GB!

## Project Expectations
For each project in Term 1, keep in mind a few key elements:

* rubric
* code
* writeup
* submission

### Rubric
Each project comes with a rubric detailing the requirements for passing the project. Project reviewers will check your project against the rubric to make sure that it meets specifications.

Before submitting your project, compare your submission against the rubric to make sure you've covered each rubric point.

Here is an example of a project rubric:

![Example of a project rubric](https://d17h27t6h515a5.cloudfront.net/topher/2017/February/5894f8b9_screen-shot-2017-02-03-at-1.39.23-pm/screen-shot-2017-02-03-at-1.39.23-pm.png)
Example of a project rubric

### Code
Every project in the term includes code that you will write. For some projects we provide code templates, often in a Jupyter notebook. For other projects, there are no code templates.

In either case, you'll need to submit your code files as part of the project. Each project has specific instructions about what files are required. Make sure that your code is commented and easy for the project reviewers to follow.

For the Jupyter notebooks, sometimes you must run all of the code cells and then export the notebook as an HTML file. The notebook will contain instructions for how to do this.

Because running the code can take anywhere from several minutes to a few hours, the HTML file allows project reviewers to see your notebook's output without having to run the code.

Even if the project requires submission of the HTML output of your Jupyter notebook, please submit the original Jupyter notebook itself, as well.

### Writeup
All of the projects in Term 1 require a writeup. The writeup is your chance to explain how you approached the project.

It is also an opportunity to show your understanding of key concepts in the program.

We have provided writeup templates for every project so that it is clear what information needs to be in each writeup. These templates can be found in each project repository, with the title `writeup_template.md`.

Your writeup report should explain how you satisfied each requirement in the project rubric.

The writeups can be turned in either as Markdown files (.md) or PDF files.

### Submission
When submitting a project, you can either submit it as a link to a [GitHub repository](https://github.com/) or as a ZIP file. When submitting a GitHub repository, we advise creating a new repository, specific to the project you are submitting.

GitHub repositories are a convenient way to organize your projects and display them to the world. A GitHub repository also has a README.md file that opens automatically when somebody visits your GitHub repository link.

As a suggestion, the README.md file for each repository can include the following information:

* a list of files contained in the repository with a brief description of each file
* any instructions someone might need for running your code
* an overview of the project

Here is an example of a README file:
![Example of a README file](https://d17h27t6h515a5.cloudfront.net/topher/2017/February/5894ff95_screen-shot-2017-02-03-at-2.08.26-pm/screen-shot-2017-02-03-at-2.08.26-pm.png)

Example of a README file

If you are unfamiliar with GitHub , Udacity has a brief [GitHub tutorial](http://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html) to get you started. Udacity also provides a more detailed free [course on git and GitHub](https://www.udacity.com/course/how-to-use-git-and-github--ud775).

To learn about REAMDE files and Markdown, Udacity provides a free [course on READMEs](https://www.udacity.com/courses/ud777), as well.

GitHub also provides a [tutorial](https://guides.github.com/features/mastering-markdown/) about creating Markdown files.

## Project Submission
Navigate to [the project repository on GitHub](https://github.com/udacity/CarND-LaneLines-P1) and have a look at the Readme file for detailed instructions on how to get setup with Python and OpenCV and how to access the Jupyter Notebook containing the project code. You will need to download, or `git clone`, this repository in order to complete the project.

In this project, you will be writing code to identify lane lines on the road, first in an image, and later in a video stream (really just a series of images). To complete this project you will use the tools you learned about in the lesson, and build upon them.

Your first goal is to write code including a series of steps (pipeline) that identify and draw the lane lines on a few test images. Once you can successfully identify the lines in an image, you can cut and paste your code into the block provided to run on a video stream.

You will then refine your pipeline with parameter tuning and by averaging and extrapolating the lines.

Finally, you'll make a brief writeup report. The github repository has a `writeup_template.md` that can be used as a guide.

Have a look at the video clip called "P1_example.mp4" in the repository to see an example of what your final output should look like. Two videos are provided for you to run your code on. These are called "solidWhiteRight.mp4" and solidYellowLeft.mp4".

### Evaluation
Once you have completed your project, use the [Project Rubric](https://review.udacity.com/#!/rubrics/322/view) to review the project. If you have covered all of the points in the rubric, then you are ready to submit! If you see room for improvement in **any** category in which you do not meet specifications, keep working!

Your project will be evaluated by a Udacity reviewer according to the same [Project Rubric](https://review.udacity.com/#!/rubrics/322/view). Your project must "meet specifications" in each category in order for your submission to pass.

### Submission
#### What to include in your submission
You may submit your project as a zip file or with a link to a github repo. The submission must include two files:

* Jupyter Notebook with your project code
* writeup report (md or pdf file)

#### Ready to submit your project?
Click on the "Submit Project" button and follow the instructions to submit!


