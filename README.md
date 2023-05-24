> **Warning**
> This is an *unsupported* and *unmaintained* prototype!

# OpenJDK Buildpacks

This are some WIP build stacks for building Java applications using supported images like Red Hat OpenJDK.

## Prerequisites

To use buildpacks the `pack` command is needed, see the instructions here on how to install it: https://buildpacks.io/docs/tools/pack/

MacOS users will also need to install `coreutils` using something like `brew install coreutils`.

## Creating Buildpacks

To install the build packs run clone this repo and run the `create-buildpacks.sh` script.

## How to build for OpenJDK

To test the buildpack for OpenJDK run this:

```
pack build openjdk-jvm-test-app --path apps/java-sample-app --builder redhat/buildpacks-builder-openjdk-jvm:latest
```

## Running the Image

After having built the image with one of the commands above you can simply run them, eg:

```
docker run -it --rm openjdk-jvm-test-app
```

## Development

The information for creating buildpacks comes from:

https://buildpacks.io/docs/buildpack-author-guide/create-buildpack/
