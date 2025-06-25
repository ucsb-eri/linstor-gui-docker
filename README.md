# LINSTOR-GUI Docker Images

## Rationale
The official linstor-gui project contains the files required to build a docker image, but unfortunately it does not provide an official build.

Initially I made a fork of the repo, to add the docker build, but this proved cumbersome:

- The Dockerfile builds a release downloaded from the web, not the git repo
- The Dockerfile only allows building the latest release (as defined by git). This release is not always available on the release website.


To circumvent these problems, I copied the required files into a separate repo, and lightly modified them so that you can build any release from the release site.

## Building a new docker image

To build a release, go to https://pkg.linbit.com/ and find the release you want. The LINSTOR-GUI files are listed under LINSTOR, with the following file format: `linstor-gui-x.x.x.tar.gz`

In this repo go to `Actions | Docker Build | Run Workflow` and type the version number you found above into the `Tag to build` field.


## Using the image

You can find all available images here: https://github.com/ucsb-eri/linstor-gui/pkgs/container/linstor-gui
