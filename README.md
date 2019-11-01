# `docker` 

## 1. Docker on Windows 10 home
* [personal history of struggling](https://github.com/jehyunlee/docker/blob/master/Win10Home/text.md)

## 2. Docker run script
```bash
docker run -it --name=geo -e DISPLAY=$DISPLAY -v //c/Arbeitplatz/:/workplace -p 8888:8888 --shm-size 2g jehyunlee/02dsml:basic_geo
```

## 3. Dockerfiles
01. [jehyunlee/00_base](https://github.com/jehyunlee/docker/blob/master/00_base)  
    * [:kr](https://github.com/jehyunlee/docker/blob/master/00_base/Dockerfile)
      * [ubuntu] `ubuntu 16.04`
      * [browser] `firefox`, `dbus-x11` 
      * [language] `fonts-nanum` `vim` `uim` `uim-byeoru`
      * [locale] `ko_KR.UTF-8`
02. [jehyunlee/01_anaconda](https://github.com/jehyunlee/docker/blob/master/01_anaconda)  
    * [:01_jlab](https://github.com/jehyunlee/docker/blob/master/01_anaconda/jlab/Dockerfile)
      * [DEV] `anaconda3`, `nodejs`
      * [ENV] `alias`
    * [:02_jlabext](https://github.com/jehyunlee/docker/blob/master/01_anaconda/jlab_ext/Dockerfile)
      * [ENV] `jupyter lab` extensions
        - [`ipywidget`](https://ipywidgets.readthedocs.io/en/latest/), [`github`](https://github.com/jupyterlab/jupyterlab-github), [~`latex`~](https://github.com/jupyterlab/jupyterlab-latex), [`drawio`](https://github.com/QuantStack/jupyterlab-drawio), [`go_to_definition`](https://github.com/krassowski/jupyterlab-go-to-definition), [`code_formatter`](https://github.com/ryantam626/jupyterlab_code_formatter), [`toc`](https://github.com/jupyterlab/jupyterlab-toc), [`google-drive`](https://github.com/jupyterlab/jupyterlab-google-drive), `git`, [`mathjax3`](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)
03. [jehyunlee/02_dsml](https://github.com/jehyunlee/docker/blob/master/02_dsml)  
    * [:01_dsml](https://github.com/jehyunlee/docker/blob/master/02_dsml/basic/Dockerfile)
      * [DEV] `tensorflow 1.14`, `keras 2.2.4`, `pytorch 1.3.0`, `hyperspy`, `selenium`, `geckodriver`
    * [:02_geocoding](https://github.com/jehyunlee/docker/blob/master/02_dsml/basic_geo/Dockerfile)
      * [DEV] [`shapely`](https://shapely.readthedocs.io/en/stable/manual.html), [`geopandas`](https://datascienceschool.net/view-notebook/ef921dc25e01437b9b5c532ba3b89b02/), [`descartes`](https://pypi.org/project/descartes/), [`folium`](https://github.com/python-visualization/folium) 
      * [ENV] `jupyter lab` extensions
        - [`geojson`](https://www.npmjs.com/package/@jupyterlab/geojson-extension)
        
