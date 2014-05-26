# quickscrape [![Build Status](https://secure.travis-ci.org/ContentMine/quickscrape.png?branch=master)](http://travis-ci.org/ContentMine/quickscrape)

Very simple extensible, headless scraping.

`quickscrape` is a simple command-line tool for scraping websites using declarative scraper definitions.

## Getting Started
Install the module with: `npm install quickscrape`.

**NOTE**: This is pre-alpha software. It works for some very specific test-cases and is under active development. Please wait until we're in beta to report issues.

## Documentation

Run `quickscrape --help` from the command line to get help:

```

  Usage: quickscrape [options]

  Options:

    -h, --help            output usage information
    -V, --version         output the version number
    -u, --url <url>       URL to scrape
    -s, --scraper <path>  Path to scraper definition (in JSON format)
    -o, --output <path>   Where to output results (directory will created if it doesn't exist) [output]

```

You must provide scraper definitions in the format used in the [ContentMine journal-scrapers](https://github.com/ContentMine/journal-scrapers).

## Examples


```
// grab some pre-cooked scraper definitions
git clone git@github.com:ContentMine/journal-scrapers.git

// scrape some journal PDFs
quickscrape \
  --url https://peerj.com/articles/384 \
  --scraper journal-scrapers/peerj.json
  --output peerj-384

quickscrape \
  --url http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0098172 \
  --scraper journal-scrapers/plosone.json
  --output plos-waspfaces
```

## Contributing

We are not yet accepting contributions, if you'd like to help please drop me an email (richard@contentmine.org) and I'll let you know when we're ready for that.

## Release History
_(Nothing yet)_

## License
Copyright (c) 2014 Richard Smith-Unna  
Licensed under the MIT license.
