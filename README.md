# Heroku Buildpack for NextWeb

[![license](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

This is a [Heroku buildpack][buildpack] for statically build NextWeb application.

## Getting Started

This buildpack assumes your application is being deployed with the following organization:

```
  + bin/
  |   next    
  + app/
  |   ...
  |   ...
  | [Procfile]
  | ...
```

The buildpack will detect your repository as NextWeb application only if NextWeb CLI (`next`) is found inside the `./bin` folder.

## Usage

Creating a new Heroku app that uses this buildpack:

```sh
$ heroku create --buildpack https://github.com/IronGeek/heroku-buildpack-nextweb.git
```

Configuring an existing Heroku app to use this buildpack:

```sh
$ heroku buildpacks:set https://github.com/IronGeek/heroku-buildpack-nextweb.git
```

## License

This project is licensed under the terms of the [MIT license](LICENSE).

[buildpack]: https://devcenter.heroku.com/articles/buildpacks
    "Heroku Dev Center article on buildpacks"