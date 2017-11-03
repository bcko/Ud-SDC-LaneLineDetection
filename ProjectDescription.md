# Project Introduction

## Finding Lane Lines in a Video Stream

[Project Instruction](https://youtu.be/LatP7XUPgIE)

### Project Instructions
To get started on the project, download or `git clone` [the project repository on GitHub](https://github.com/udacity/CarND-LaneLines-P1). You'll find the instructions in the README file. Click "Next" below to view information about setting up the project on your computer.

# Starter Kit Installation
In this term, you'll use Python 3 for programming quizzes, labs, and projects. The following will guide you through setting up the programming environment on your local machine.

There are two ways to get up and running:
1. Anaconda
2. Docker

We recommend you first try setting up your environment with Anaconda. It's faster to get up and running and has fewer moving parts.

If the Anaconda installation gives you trouble, try Docker instead.

Follow the instructions in [this README](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md).

Here is a great link for learning more about [Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111)

# Run Some Code!
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

## Troubleshooting
### ffmpeg
**NOTE**: If you don't have `ffmpeg` installed on your computer you'll have to install it for `moviepy` to work. If this is the case you'll be prompted by an error in the notebook. You can easily install `ffmpeg` by running the following in a code cell in the notebook.

```python
import imageio
imageio.plugins.ffmpeg.download()
```

Once it's installed, `moviepy` should work.

### Docker
To get the latest version of the [docker image](https://hub.docker.com/r/udacity/carnd-term1-starter-kit/), you may need to run:
```bash
docker pull udacity/carnd-term1-starter-kit
```

Warning! The image is ~2GB!

