# Description

Docker image with Python pylab packages and Jupyter Notebook in it.

# Usage

You can use it with Docker directly:
```sh
docker run --rm -it -p 8888:8888 -v $(pwd):/usr/src/app tarhan/pylab-notebook
```

Or create simple Docker Compose config file like this one:
```yaml
version: '2'
services:
  notebook:
    image: pylab-notebook
    volumes:
      - .:/usr/src/app
    ports:
      - "8888:8888"
```

In both cases you are mouting your current folder as root of notebooks tree.  

And don't forget to bind image port to some your host machine port.
