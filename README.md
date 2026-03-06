# Aropixel Admin Dev Stack

## Philosophy

The `AropixelAdminBundle` is built with a specific philosophy: it is a **toolbox** for developers, not a black-box framework like `EasyAdminBundle`. It provides the framework and tools to build an admin interface quickly while ensuring you retain full control over your code.

As a facilitator, it helps automate repetitive CRUD tasks through a custom `make:crud` generator that starts from your own `FormType`.

## Before you start coding

### Requirements

A Docker environment is provided and requires you to have these tools available:

* Docker
* Bash
* PHP >= 8.1
* [Castor](https://github.com/jolicode/castor#installation)

#### Castor

Once castor is installed, in order to improve your usage of castor scripts, you
can install console autocompletion script.

If you are using bash:

```bash
castor completion | sudo tee /etc/bash_completion.d/castor
```

If you are using something else, please refer to your shell documentation. You
may need to use `castor completion > /to/somewhere`.

Castor supports completion for `bash`, `zsh` & `fish` shells.

### Docker environment

The Docker infrastructure provides a web stack with:
- NGINX
- Mysql
- PHP
- A container with some tooling:
    - Composer
    - Node
    - Yarn / NPM

## Start coding !!

### The first time : build the stack

Build & launch the stack by running this command:

```bash
castor start
```

> [!NOTE]
> the first start of the stack should take a few minutes.

The build install your symfony app and clone all the Aropixel Admin bundles.  
The site is now accessible at the hostnames your have configured over HTTPS
(you may need to accept self-signed SSL certificate if you do not have mkcert
installed on your computer - see below).

### Take a rest

You need to go home. Take a rest !  
Stop your contributing stack by running this command:

```bash
castor stop
```


### Get back

We knew you would come back.  
Start your contributing stack again by running this command:

```bash
castor up
```

## Documentation

* [Aropixel Admin Bundle Documentation](aropixel/AdminBundle/doc/index.md)
* [CRUD Generator Documentation](aropixel/AdminBundle/doc/make_crud.md)
