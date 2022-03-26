# Node Package Purge

Removing unused packages made easier! A shell script to list unused external packages across the scope of a Node-based project.

## Usage

Mac users need to install `jq` utility using Homebrew before using the script. Run `cask install jq` or do a quick search to see how it is done if you face any issues.

To use this script, simply run it using `bash purge.sh /project_root_directory_path`

## Working

The script is really simple. It gets the list of packages installed from `package.json` of the project root and checks iteratively every file having one of the extensions from: `*.js`, `*.ts` or `*.json` using `grep` for search.

## Why

`npm` does not provide a straightforward way to list and manage unused packages. Therefore, the only way to check usage of packages is to iterate over all the project files.

Sometimes we install packages we don't end up using in the final product. This script checks the project directory passed to it for usages of all the packages and lists the number of times each package is used.