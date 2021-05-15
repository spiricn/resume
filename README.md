#### 1) Build a docker image
```sh
(cd docker && docker build . -t cv)
```

#### 2) Run a container
```sh
docker run -it -v `pwd`:/workspace cv
```

#### 3) Build the CV PDF
```sh
(cd /workspace && lualatex Nikola_Spiric_CV.tex)
```
