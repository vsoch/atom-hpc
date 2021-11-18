# Atom HPC

An [atom editor](https://atom.io/) optimized for using on HPC, meaning we will pull and run a Singularity container!
But since I'm lazy, let's push to a Docker (OCI) registry and pull from there.


## Usage

To build locally with docker:

```bash
$ docker build -t atom-hpc .
```

And then push to the repository to trigger the automated build.

## Thanks

This is based on a version from [docker-atom-editor](https://github.com/jamesnetherton/docker-atom-editor)
but updated for a specific ubuntu container and automated GitHub packages build. The commit history is maintained
to give due credit.
