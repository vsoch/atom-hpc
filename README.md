# Atom HPC

An [atom editor](https://atom.io/) optimized for using on HPC, meaning we will pull and run a Singularity container!
But since I'm lazy, let's push to a Docker (OCI) registry and pull from there.


## Usage

To build locally with docker:

```bash
$ docker build -t atom-hpc .
```

And then push to the repository to trigger the automated build. Then on your
cluster:

```bash
$ singularity pull docker://ghcr.io/vsoch/atom-hpc:v1.58.0
```
Make sure that you have `SINGULARITY_CACHEDIR` set to somewhere other than home (scratch or workspace)
so your home doesn't fill up with layers! Then run the container:

```bash
$ ./atom-hpc_v1.58.0.sif
```

This is fairly slow - a better recommendation is to use [remote atom](https://atom.io/packages/remote-atom).

## Thanks

This is based on a version from [docker-atom-editor](https://github.com/jamesnetherton/docker-atom-editor)
but updated for a specific ubuntu container and automated GitHub packages build. The commit history is maintained
to give due credit.
