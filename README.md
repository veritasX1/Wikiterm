# Wikiterm

Wikiterm is a simple terminal-based Wikipedia downloader for Linux.

It downloads articles from the German Wikipedia, converts them into clean
plain-text files and opens them directly in Nano.

## Features

- Downloads articles from the German Wikipedia
- Converts Wikipedia pages into clean plain text
- Removes web-page elements such as "Edit" and navigation controls
- Wikipedia links are highlighted in Nano
- No visible `[[ ]]` link markup in the article text
- Automatic line wrapping at 78 characters
- Internal links are listed at the end of each article
- UTF-8 text files
- No additional Python packages required
- Designed for offline archiving and removable media

## Requirements

- Ubuntu or another Linux distribution
- Python 3
- Nano
- Internet connection for downloading articles

## Installation

### 1. Download Wikiterm

Clone the repository:

    git clone https://github.com/veritasX1/Wikiterm.git

Enter the directory:

    cd Wikiterm

### 2. Install Wikiterm

Copy the program to your personal executable directory:

    mkdir -p ~/.local/bin
    cp wikipedia ~/.local/bin/wikipedia
    chmod +x ~/.local/bin/wikipedia

### 3. Make sure ~/.local/bin is in your PATH

On most modern Ubuntu installations this is already the case.

You can check with:

    echo $PATH

If `~/.local/bin` is not listed, add it with:

    echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
    source ~/.bashrc

### 4. Test the installation

Run:

    wikipedia download Bremen

Wikiterm will download the article and open it automatically in Nano.

## Usage

Download an article:

    wikipedia download Bremen

Other examples:

    wikipedia download Berlin

    wikipedia download "Windows 3.11"

    wikipedia download "Albert Einstein"

    wikipedia download Linux

Downloaded articles are stored in:

    ~/Dokumente/Wikipedia/

For example:

    ~/Dokumente/Wikipedia/Bremen.txt

## Wikipedia links

Links to other Wikipedia articles are highlighted when the article is
opened in Nano.

The link markup is not displayed.

For example, the downloaded article contains:

    Bremen liegt an der Weser.

rather than:

    Bremen liegt an der [[Weser]].

A list of the internal Wikipedia links found in the article is included
at the end of the text file.

## Example

Running:

    wikipedia download Bremen

creates:

    ~/Dokumente/Wikipedia/Bremen.txt

The file contains the article in a simple text format suitable for
reading in Nano or archiving as a plain-text file.

## Offline archive

Because Wikiterm creates ordinary `.txt` files, downloaded articles can
easily be copied to external storage.

For example:

    cp ~/Dokumente/Wikipedia/Bremen.txt /media/$USER/DISKETTE/

This makes it possible to build a personal offline Wikipedia archive.

## License

Wikiterm is released under the MIT License.

Wikipedia content is provided by the Wikimedia Foundation and its
contributors and is subject to the applicable Wikipedia licenses.

For information about Wikipedia's licensing terms, see:

https://de.wikipedia.org/wiki/Wikipedia:Lizenzbestimmungen
