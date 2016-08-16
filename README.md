# Golang Version Management with goenv

[![Build Status](https://travis-ci.org/kaneshin/goenv.svg?branch=master)](https://travis-ci.org/kaneshin/goenv)

goenv supplies the management system to switch between multiple golang releases.

## Installation

### Checkout

Clone the repository to install the latest version of goenv.

```shell
git clone https://github.com/kaneshin/goenv.git ~/.goenv
```

Define the cloned repository path as `$GOENV_ROOT` and then add `$GOENV_ROOT/bin` to your `$PATH` for access to the goenv command-line utility.

```shell
export GOENV_ROOT="$HOME/.goenv"
export PATH="$GOENV_ROOT/bin:$PATH"
```

Add `goenv init` to your shell to enable shims.

```shell
eval "$(goenv init -)"
```

## Usage

```
$ goenv help
Usage: goenv <command> [<args>]

Some useful goenv commands are:
   exec        Execute a command from a particular Go version.
   shell       Set GOENV_VERSION for the lifetime of a shell.
   local       Persist the preferred Go version in the cwd.
   global      Persist the preferred Go default version.
   install     Install a version of Go.
   uninstall   Uninstall a version of Go.
   version     Show the current Go version.
   versions    Display all versions of Go installed in `${GOENV_ROOT}/versions/*'.
   rehash      Rehash goenv shims (run this after installing executables)

See `goenv help <command>' for information on a specific command.
```

## Credits

This library was heavily, heavily, heavily inspired by
[@sstephenson](https://github.com/sstephenson)'s
[rbenv](https://github.com/sstephenson/rbenv) and
[ruby-build](https://github.com/sstephenson/ruby-build) projects.
A few ideas were also taken from [nvm](https://github.com/creationix/nvm).

A number of patterns and utilities are borrowed from that project,
and it is my hope that goenv provides the same simplicity,
elegance, and usability that I've come to love in rbenv and ruby-build
for Go users.
