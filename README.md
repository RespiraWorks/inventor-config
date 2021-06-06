# Inventor configuration

This repository contains Autodesk Inventor configuration and templates for mechanical design aspects of RespiraWorks' projects. This document  also explains how to install and configure your Inventor to best collaborate with our team. If you are part of the mechanical team or will be contributing to the mechanical design in any way, you should follow this guide and use this repository to help you.

Assumptions:
* all of our projects or products requiring mechanical design should use the same configuration
* however, parts and assemblies can be viewed and used by external persons/organizations without these configurations

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

### Configure inventor defaults

Please configure your inventor to use metric (mm) by default. You might be creating tubing and other sketch-based parts, which may get generated in imperial, which is not what we want.

For how to configure the default template to use mm, read [this article](https://knowledge.autodesk.com/support/inventor/learn-explore/caas/sfdcarticles/sfdcarticles/How-to-switch-the-default-units-from-imperial-to-metric-in-Inventor.html).

### Enable Content Center

Some hardware in our models comes from the Inventor Content Center.

If you are not finding the parts in the Content Center, it maybe that your Inventor is out of date. Also, there is an [article](https://knowledge.autodesk.com/support/inventor/troubleshooting/caas/sfdcarticles/sfdcarticles/Inventor-Content-Center-libraries-are-empty.html) explaining some possible solutions.

### Install threadModeler

You may have to create in-model threads for interfacing custom 3d printed parts with hardware, pneumatic components or sensors. In this case, you may find it useful to install the threadModeler plugin. Read more about this (optional) step in [this guide](thread_modeler.md). 

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

You can now go back to the main [wiki](https://github.com/RespiraWorks/Ventilator/wiki) and read the rest of whatever
is pertinent to your specific work.
