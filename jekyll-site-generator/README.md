#Jekyll Site Generator

To build the image
```
docker build . -t jekyll-generator
```

To run the image
```
docker run --rm -it -p 4000:4000 -v <local site dir>:/site jekyll-generator /bin/bash
```
Once the container starts run the following
```
bundle
```
to install all the dependencies, and then 
```
bundle exec jekyll serve --host 0.0.0.0
```
You shold now be able to access the jekyll instance at http://localhost:4000
