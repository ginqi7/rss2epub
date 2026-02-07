[![README-简体中文](https://img.shields.io/badge/README-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-555555.svg)](https://github.com/ginqi7/rss2epub/blob/master/README.zh-CN.md)


A tool that converts RSS content into ePub format ebooks.

# Usage

- Build rss2epub using [Maven](http://maven.apache.org). Please install Maven beforehand.
- Execute the command in the rss2pub directory.

  ```bash
  mvn package
  ```

The rss2epub JAR package is compiled in the target directory after building.

- Instructions for using the package:

  ```bash
  java -jar rss2epub.jar config-file output-file
  ```

For instance, run the command in the rss2epub directory:

  ```bash
  java -jar target/rss2epub-0.0.1-SNAPSHOT-all.jar book.yml book.epub
  ```


It will generate an eBook titled book.epub.

# Configuration

The configuration type used in rss2epub is [YAML](http://www.yaml.org). The structure is:

```bash
title: The title of eBook
author: The author of eBook
image: If fetching online images
feeds:
    - Feed URL
    - Feed URL
    ...
    - Feed URL
```

You can refer to the book.yml file located in the project's root directory.

# Features

- Lightweight and easy to use.
- Automatic image processing.
- Automatically generate index.
- A pure command-line tool that does not rely on other eBook management tools, making it convenient for integration with other scripts.

# Dependencies

- [Log4j](http://logging.apache.org/log4j/1.2/) - Logging Library
- [SnakeYAML](https://code.google.com/p/snakeyaml/) - A library for parsing YAML files.
- [Rome](https://rometools.jira.com/wiki/display/ROME/Home) - A tool for reading and parsing RSS feeds.
- [Epublib](http://www.siegmann.nl/epublib) - A tool for generating EPUB format eBooks (no longer maintained).
- [epub4j](https://github.com/documentnode/epub4j) A java library for reading/writing/manipulating EPUB files, with improvements based on epublib.

Maven automatically handles these dependencies, so you don't need to explicitly manage them when compiling and running your program.

This list is solely an expression of gratitude for these items.
