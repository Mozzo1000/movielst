# movielst [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) [![PyPI version](https://badge.fury.io/py/movielst.svg)](https://badge.fury.io/py/movielst)

movielst is based on [moviemon](https://github.com/iCHAIT/moviemon) , a Python application that displays information about all your movies in the command line.
movielst will index movies in a selected directory, retrieve and display information like IMDb rating, release date, top casts and more.
This fork is intended to update the project to latest python version, fix existing issues from the original project and add new features.

![](https://i.imgur.com/Lb8qCXa.gif)

## Features
* Export to csv and xlsx file
* Use either OMDb(default) or TMDb API to retrieve movie information
* Web interface
* Edit index file from commmand line

## Installation
#### Install latest stable with pip
`pip install movielst`
#### Install from source with pip
`pip install git+git://github.com/Mozzo1000/movielst.git`


## Dependencies

CLI :
* [guessit](https://github.com/guessit-io/guessit) - Retrieving correct movie name from files.
* [terminaltables](https://github.com/Robpol86/terminaltables) - Printing out tables nicely.
* [tqdm](https://github.com/tqdm/tqdm) - Showing a progressbar when indexing movies.
* [colorama](https://github.com/tartley/colorama) - Coloring outputs.
* [XlsxWriter](https://github.com/jmcnamara/XlsxWriter) - Exporting table to excel.

Web :
* [Flask](https://github.com/pallets/flask) - Web framework
* [Flask-WTF](https://github.com/lepture/flask-wtf) - Easier form handling

## Usage:
```sh
  movielst PATH
  movielst [-i | -t | -g | -a | -c | -d | -y | -r | [-e type output] | -f | -I | -T | -ec | -ed]
  movielst -h | --help
  movielst --version
  movielst_web
```

### Options:
```sh
  -h, --help            Show this screen.
  -v, --version             Show version.
  PATH                  Path to movies dir. to index/reindex all movies.
  -i, --imdb            Sort acc. to IMDB rating.(dec)
  -t, --tomato          Sort acc. to Tomato Rotten rating.(dec)
  -g, --genre           Show movie name with its genre.
  -a, --awards          Show movie name with awards received.
  -c, --cast            Show movie name with its cast.
  -d, --director        Show movie name with its director(s).
  -y, --year            Show movie name with its release date.
  -r, --runtime         Show movie name with its runtime.
  -e type output, --export type output
                        Export list to either csv or excel
  -f, --force           Force indexing
  -I, --imdb-rev        Sort acc. to IMDB rating.(inc)
  -T, --tomato-rev      Sort acc. to Tomato Rotten rating.(inc)
  -ec, --edit-config    Open the configuration file in the default editor
  -ed, --edit-index     Edit the index file
```

## Credits
[iCHAIT](https://github.com/iCHAIT) - Original developer

## Contribute

Found a bug or want to suggest a new feature? Report it by opening an issue. Feel free to send a pull request for any improvements or feature requests ;)


## License
`movielst` is released under the [MIT License](http://www.opensource.org/licenses/MIT).