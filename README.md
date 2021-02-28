# Automation of Intelligence Preparation of the Battleﬁeld

In military operations armed forces have to get a better idea of the area in which they have to operate including terrain features, threats and avenues of approach. So they gather intelligence on the location, enemy, weather, vegetation, infrastructure and many such factors before making decisions. Intelligence Preparation of the Battleﬁeld (IPB) is the name given for that process of analyzing the situation and making decisions based on predictions. Usually this process happen manually by ofﬁcers using hard copy maps and it have number of inconveniences. We implement and present a set of algorithms, tools and approaches for automating terrain analysis and decision making in Intelligence Preparation of the Battleﬁeld process. The implementation is found here. 

The implementation consist of two systems IPBBackend (consist of the backend server with IPB algorithms) and IPBFrontend (consist of web application UI)

If you want to set-up the system follow the steps below.

## Setup

You need a latest git version supporting git lfs to clone the repo as it contain heavy files. ([git lfs](https://git-lfs.github.com/))

First clone the repo with

```bash
git clone https://github.com/cepdnaclk/e14-4yp-ipb.git
```
If this gives an error saying lfs quota has exceeded, That means the large files cannot be cloned, but remaining files will be cloned as needed.

But you need the below set of large files. So download them from the given links and put them in the correct locations mentioned with them. (Check whether below files are there in cloned files. They must be larger than 100Mb. If not, download and replace)

[roads.geojson](https://gitlab.com/intelligence-preparation-of-the-battlefield/ipb-software/overlaybackend/-/raw/master/srilankadata/roads.geojson) - IPBBackEnd/srilankadata/

[elevation](https://gitlab.com/intelligence-preparation-of-the-battlefield/ipb-software/overlaybackend/-/raw/master/srilankadata/elevation.geojson) - IPBBackEnd/srilankadata/

[buildings.geojson](https://gitlab.com/intelligence-preparation-of-the-battlefield/ipb-software/overlaybackend/-/raw/master/srilankadata/buildings.geojson) - IPBBackEnd/srilankadata/

[srilankaterrain.tif](https://gitlab.com/intelligence-preparation-of-the-battlefield/ipb-software/overlaybackend/-/raw/master/mobility/srilankaterrain.tif) - IPBBackEnd/mobility/

## Prerequisites

Below python interpreter and pythons libraries must be installed for using this tool.

- Python (3.7 recommended)
- GDAL (A python library - [https://gdal.org/](https://gdal.org/))- see [video](https://youtu.be/3COTt03Rd3M) how to install as python library
- Python Flask ([https://flask.palletsprojects.com](https://flask.palletsprojects.com))
- flask_RESTful
- flask_cors
- numpy
- scikit-image

## How to Run

Then to run the start backend run below command in IPBBackEnd folder.

```python
python init.py
```

To start running the frontend, run map.html in IPBFrontEnd
