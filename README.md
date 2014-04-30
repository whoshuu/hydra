# hydra

A script for managing Python versions. This tool lets you keep all of your development versions of Python in a single location that is accessible even without `root` privileges. Hydra lets you bootstrap a new development machine quickly and painlessly, with as few dependencies as possible and without ever reaching into `sudo` territory.

## Installing

With pip:

```bash
> pip install hydrapy
> hydra version
Your current version of hydra is 0.0.1.
```

To install hydra from source, it is only necessary to put the `hydra` script into a directory that's in your `PATH`. Once there, you'll have full access to everything hydra can do.

Optionally, since `PATH`'s are usually in only `root`-accessible, you can simply `source $PATH/TO/HYDRA/SCRIPT` in your `.bashrc` or from the terminal to load the script.

## Commands

```bash
> hydra install [version]
```

Installs the specified version of Python into your `HYDRA_HOME_DIRECTORY`, which by default is `$HOME/.hydra`. For instance, calling `hydra install 2.7.6` will download and compile `Python-2.7.6` into a directory called `2.7.6` in `HYDRA_HOME_DIRECTORY`. The Python executable will be available in the `bin` subdirectory.

```bash
> hydra uninstall [version]
```

Uninstalls the specified version of Python from your `HYDRA_HOME_DIRECTORY`. For instance, calling `hydra uninstall 2.7.6` will delete the directory called `2.7.6` from `HYDRA_HOME_DIRECTORY`. If a virtualenv is found to be using links to libraries or modules in that directory, confirmation of the deletion will be required.

```bash
> hydra list
```

Lists all versions of Python installed using hydra. An optional `-a` or `--all` flag may be passed in to list all available versions of Python that may be installed.

```bash
> hydra version
```

Prints the version of hydra currently installed.

```bash
> hydra help
```

Displays the list of available commands and further usage guidelines.

## Recommended Use

It is highly recommended that hydra be used in conjunction with [virtualenv](http://www.virtualenv.org/en/latest/) and [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/).

## Contributing

Please fork this repository and contribute back using [pull requests](https://github.com/whoshuu/hydra/pulls). Features can be requested using [issues](https://github.com/whoshuu/hydra/issues). All code, comments, and critiques are greatly appreciated.
