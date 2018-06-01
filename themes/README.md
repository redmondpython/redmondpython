# Prototype for RedmondPython.com

A prototype I threw together as a possible alternative for the RP site using hexo.

## Setup

1. Download and install [Node.js](https://nodejs.org/en/).
2. Run:
    ```bash
    $ git clone https://github.com/mkpt/rp2018.git
    $ cd rp2018
    $ sudo npm install
    $ npm install --save hexo-renderer-scss
    $ hexo generate
    $ hexo server
    ```

## Usage

### Page

Create a new page:
```
$ hexo new page my-page-title
```
This creates a new folder under `source`. Put your content under `my-page-title/index.md`.

When finished, generate and start the built-in server:
```
$ hexo generate
$ hexo server
```
It's at [localhost:4000](localhost:4000).

To add your page to the hamburger menu, add it to the `config.yml` under `themes/hexo-theme-phantom-master`:
```yml
menu:
  Home: /
  Onboarding: /onboarding
  Windows Setup: /setupwindows
  Mac Setup: /setupmac
  Linux Setup: /setuplinux
  Workshop: /workshop
  Practice: /practice
  Projects: /projects
  Contributing: /about
  Archives: /archives
  My New Page: /my-page-title
```
### Post

Create a new post:
```
$ hexo new post DD-mon-YYYY
```
Follow the existing post formats. Need a square image of Seattle at least 450x450.

When finished, generate and start the built-in server:
```
$ hexo generate
$ hexo server
```
It's at [localhost:4000](localhost:4000).

## Issues

Hit me up.
