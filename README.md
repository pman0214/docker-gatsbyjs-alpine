# pman0214/gatsbyjs-alpine

> GatsbyJS Development on Alpine

[![Docker Build](https://img.shields.io/docker/cloud/automated/pman0214/gatsbyjs-alpine.svg)](https://hub.docker.com/r/pman0214/gatsbyjs-alpine/)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

Development environment for [Gatsby](https://www.gatsbyjs.org), [React](https://reactjs.org)-based static site generator.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Content](#content)
- [Contribute](#contribute)
- [License](#license)

## Install

```bash
docker pull pman0214/gatsbyjs-alpine
```

## Usage

Default WORKDIR is ``/app``.

```bash
$ docker run --rm -it -v $PWD:/app pman0214/gatsbyjs-alpine 'gatsby new myapp https://github.com/gatsbyjs/gatsby-starter-default'
$ docker run --rm -it -p 8000:8000 -v $PWD/myapp:/app pman0214/gatsbyjs-alpine 'gatsby develop --host=0.0.0.0'
```

## Content

This docker image is based on [Node.js official docker image](https://hub.docker.com/_/node).
The image contains:

* node.js
* gatsby-cli
* git (to use starter)
* python3 (for gatsby-remark-images->gatsby-plugin-sharp->sharp->node-gyp)
* gcc, g++, make (for some node.js modules)

## Contribute

* Bugfix Pull requests are welcome.
* If you have a request to include/exclude packages on this docker image, please make an issue on GitHub and discuss.
Pull requests after the discussion are welcome.

## License

This Docker image is released under the BSD 3-clause license.
See ``LICENSE.txt``.

* Copyright (c) 2020 Shigemi ISHIDA
