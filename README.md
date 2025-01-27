# Meal Planner
> The Meal Planner is a digital voice assistant based on Rasa that helps you with the everyday tasks such as buying ingredients, preparing meals and finding recipes.

## Table of contents
* [General info](#general-info)
* [Git workflow](#git-workflow)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)

## General info
The repository was initialized with the base code of Rasa's default startup project.

## Git workflow
Feature branch workflow
1. Clone project:
```
$ git clone https://github.com/pedroggbcampos/rasa-project
```
2. Create branch with your feature:
```
$ git checkout -b $feature_name
```
3. Write code and then stage all tracked, modified files before the commit:
```
$ git add *
```
4. Commit changes:
```
$ git commit -m "Add x feature and correct file y"
```
5. Push your branch:
```
$ git push origin $feature_name
```
6. Review your code on commits page.

7. Create a merge request.

8. Your team lead will review the code & merge it to the main branch.

9. If project is not finished, go back to step 2.

To know more about this workflow watch the video [Understanding the Feature Branch Workflow](https://www.youtube.com/watch?v=JUpKDkb4Zhc&ab_channel=TechSnips)

**IMPORTANT:**
After opening your laptop to work on the project, make sure you pull the latest version of the master branch into your feature branch!
Do this often before starting to work or whenever you think someone updated the master. This avoids many merge conflicts. To do this you do:
```
$ git checkout master
$ git fetch
$ git pull --rebase origin master
$ git checkout $feature_name
$ git rebase master
```

With these lines of code you get the latest master. Then you go back to your previous branch and rebase your branch with the latest master.
To know more details on this refer to the [Guide for no merge conflicts](https://geshan.com.np/blog/2016/04/3-simple-rules-for-less-or-no-git-conflicts/)

## Technologies
* Python - version 3.7.9
* Rasa - version 2.1.1

## Setup (Linux)
If you want to use with conda which is recommended, firstly install miniconda. See the [miniconda install instructions](https://docs.conda.io/en/latest/miniconda.html)
```
$ conda create -n rasa-lab python=3.7
$ pip install rasa
$ rasa --version
$ rasa init
```

## Running the system with Rasa Shell (Linux)
In order to run rasa shell you'll need three terminal windows open, two with different servers running and a third with the rasa shell. We should fix this so it's more convenient

You need [docker](https://www.docker.com) installed. In one terminal, run:
```
$ docker run -p 8000:8000 rasa/duckling
```
In a second terminal, go to the project folder and run:
```
$ rasa run actions
```
In a third terminal, go to the project folder and run:
```
$ rasa train       (only needed the first time or after changes)
$ rasa shell
```

## Features
List of ready features:
* Awesome feature 1
* Awesome feature 2
* Awesome feature 3

To-do list:
* Wow improvement to be done 1
* Wow improvement to be done 2

## Status
Project is: _in progress_
