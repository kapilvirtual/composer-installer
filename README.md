# composer-installer

## Usage
The composer-installer plugin will run automatically when setup within a module project.

At present there is one supported type, lucidity-module. In future there may be additional module types 

### lucidity-module
lucidity-module modules are installed within the top-level of your project, within the `modules` folder. 

To setup up your module to be installed using the lucidity-module format, the following details need to be added to your `composer.json`

```
{
    "type": "lucidity-module",
    "require": {
        "luciditysoftware/lucidity-composer-installer": "1.0.0"
     }
}

```


## Local Development
To take advantage of symlinking to within your local development environment, you'll need to perform a bit of setup. 

Add the following environment variable to your .bash_profile (or similar)

```
COMPOSER_ENABLE_LOCAL_MODULES=true
```

By default, composer-installer will look for matching packages in the directory above your working directory (e.g. /workspace/web would scan the /workspace directory for matching packages).

If you wish to use a different directory, you can supply that using the environment variable `COMPOSER_MODULE_DIRECTORY`, either within your .bash_profile or on the cli at runtime.

