A place where my personal resume is stored (`in source code`).

To build the resume as a PDF file, **lualatex** may be used. A **Dockerfile** describing the environment  needed to do so, is stored in the `/docker` directory.

[For a pre-built PDF see the release page](https://github.com/spiricn/resume/releases/latest)

---

Build instructions:

##### 1) Build a docker image

```sh

(cd docker && docker build . -t spiricn-resume)

```



##### 2) Spawn a container

```sh

docker run -it -v `pwd`:/workspace spiricn-resume

```



##### 3) Build the resume PDF

```sh

(cd /workspace && lualatex Nikola_Spiric_CV.tex)

```