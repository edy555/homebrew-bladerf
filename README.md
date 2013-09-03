homebrew-bladerf
=================

# Installation

Tested on Mountain Lion 10.8 with Xcode 4.6.

  * Prepare homebrew

        $ curl -fsSk https://raw.github.com/mxcl/homebrew/go | ruby

  * Install bladerf with brew

        $ brew tap edy555/bladerf
        $ brew install bladerf --HEAD

# Installing GNURadio and gr-osmosdr

- Install XQuartz

Download XQuartz installer XQuartz-2.7.4.dmg from
http://xquartz.macosforge.org/landing/, then install it.

- Install the python package prerequisites

  ```sh
  brew install python gfortran umfpack swig
  ```

- Install the prerequisite python packages

  ```sh
  pip install numpy scipy Cheetah lxml
  export PKG_CONFIG_PATH="/usr/x11/lib/pkgconfig" pip install http://downloads.sourceforge.net/project/matplotlib/matplotlib/matplotlib-1.1.1/matplotlib-1.1.1.tar.gz
  ```

- Before installing `gnuradio`, install `wxmac` 2.9 with python bindings

  ```sh
  brew install wxmac --python
  ```

  ```sh
  brew tap titanous/homebrew-gnuradio
  brew install gnuradio
  ```
- Create the `~/.gnuradio/config.conf` config file for custom block support

  ```ini
  [grc]
  local_blocks_path=/usr/local/share/gnuradio/grc/blocks
  ```

- Install gr-osmosdr

  ```sh
  brew install gr-osmosdr --HEAD
  ```

# Credit

  * https://github.com/titanous/homebrew-gnuradio
  * Homebrew formula for bladeRF is written by edy555 (TT)

[EOF]