# Inventor configuration

This repository contains Autodesk Inventor configuration and templates for mechanical design aspects of [RespiraWorks](https://respira.works/)' projects. This document  also explains how to install and configure your Inventor to best collaborate with our team. If you are part of the mechanical team or will be contributing to the mechanical design in any way, you should follow this guide and use this repository to help you.

Assumptions:
* all of our mechanical designs should use the same Inventor configurations, standards and templates
* however, product parts and assemblies should be easily viewed and used by external persons/organizations without these configurations

Therefore, this information is stored in this repository, separate from
[Ventilator](https://github.com/RespiraWorks/Ventilator). 

This repository constitutes an Inventor "project". You should use this repository to configure your Inventor to help you collaborate with the team in a more synchronized way.

## Install Inventor

* get credentials to our Google suite (ask team leads)
* configure your @respira.works email as described [here](https://docs.google.com/document/d/1z49daVwK5BODKR17yKRd85mAhRE2YoR_AhgDTajkC7Q/edit).
* use this email to register an account with Autodesk
* ask Curtis to get you an Autodesk license
* install and update using the Autodesk Desktop App
* install the latest version of Inventor Professional, keep it updated

## Install and configure git

Before we proceed, we assume that you have installed, configured and at least minimally learned how to use git and git bash. If not, please read the [git setup](https://github.com/RespiraWorks/Ventilator/wiki/git-setup) wiki article.

## Configure Inventor directories

First set the Inventor "Project folder". This should be some directory that is easy for you to reach by both -
your file browser and via git bash.

Follow `Tools tab` > `Application Option` > `File tab`.

Find the `Projects folder` line and set some path you will find convenient.

## Clone this repository

You should close this repository into the `Projects folder` you configured above, but you should name it something else.
This is so you can easily `cd` to it in terminal, and to the constituent "projects" such as the Ventilator that will
be subdirectories.

My recommendation is `respira` in which case you should clone it thusly:

`git clone git@github.com:RespiraWorks/inventor-config.git respira`

Open inventor and make sure you have the `RespiraWorks` project available to you. You should also be able to access
the included templates, including drawing templates.

## Customizing

`Old Versions To Keep On Save` is set to `0`. We are assuming that you are saving and then committing your
work to repo to keep the intermediate work available to your colleagues. If you do want to keep additional
versions available to yourself locally, you can set this to some non-zero value. Our repositories are configured
to ignore the `OldVersions` folders on your disk, so you do not risk polluting or blowing up our repos.

## Working on Ventilator or something...

So now we want to work on an actual project.
We have here defined a "Project" in Inventor parlance on the scope of our organization, because we want to
follow common templates, styles, color schemes, etc.. For us, however, an actual project that follows these
standards is of a level below that. So, we will want to clone something like the
[Ventilator](https://github.com/RespiraWorks/Ventilator) repository into this all-encompassing project workspace.

Use `git bash` and `cd` into the project directory where you cloned this repository. If you followed the suggestion
above, this would be `respira`. Clone the ventilator repo here:

`git clone git@github.com:RespiraWorks/Ventilator.git ventilator`

This repo is set up to ignore `Ventilator` or `ventilator` subdirectories, so there should be no conflict between
the repos on whom the files belong to.

Things should now be wonderful, and you should be seeing rainbows 'n stuff.

## What's next?

You have most things configured, but you may want to also read our ["Inventor how-to" wiki](https://github.com/RespiraWorks/inventor-config/wiki). There are a few more potential configuration steps depending on what you will work on. It may also answer some questions you are likely to have on how to use Inventor.

You can now go back to the main [Ventilator wiki](https://github.com/RespiraWorks/Ventilator/wiki) and read the rest of whatever is pertinent to your work.
