# teaching-cppcheck
Slides, references, and code for hands-on experiments with Cppcheck, a static analysis tool for C and C++ programs.

# Running CppCheck in a Docker container
To run CppCheck without installing anything, we'll use the Docker image created by [Georgy Komarov](https://github.com/jubnzv) and made available through this [GitHub repository](https://github.com/jubnzv/cppcheck-docker). 

To build the image from the source, issue:

```shell
git clone https://github.com/jubnzv/cppcheck-docker
cd cppcheck-docker
docker build -t jubnzv1/cppcheck .
```

To use the image, simply do:

```shell
docker run --rm -t -v $(pwd):/src jubnzv1/cppcheck
```

or something like

```shell
docker run --rm -t -v $(pwd):/src jubnzv1/cppcheck --addon=misra.py
```

if you want to pass optional arguments to `cppcheck`. 
