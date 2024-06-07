Hướng dẫn cài đặt và build HTML
===============================
Tham khảo list video: https://www.youtube.com/playlist?list=PLPDCBPbzk1AYghqYazE7Cxt3p7edml8I7

Tải các phần mềm:
------------------
* python
    * Cài đặt phần mềm
    * Khai báo Windows PATH environment variable
* VScode
* Cài make
    * Vào trang https://code.visualstudio.com/docs/cpp/config-mingw
        * Installing the MinGW-w64 toolchain
            * https://github.com/msys2/msys2-installer/releases/download/2024-01-13/msys2-x86_64-20240113.exe
                * sau đó run 
                    ``pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain``
            * Add the path to your MinGW-w64 bin folder to the Windows PATH environment variable by using the    following steps:

                * In the Windows search bar, type Settings to open your Windows Settings.
                * Search for Edit environment variables for your account.
                * In your User variables, select the Path variable and then select Edit.
                * Select New and add the MinGW-w64 destination folder you recorded during the installation   process to the list. If you used the default settings above, then this will be the path:  C:\msys64\ucrt64\bin.
                * Select OK to save the updated PATH. You will need to reopen any console windows for the new    PATH location to be available.

Chạy các lệnh cmd:
------------------
* ``pip install sphinx``
* ``pip install sphinx_theme``
* ``mingw32-make html``
* ``pip install sphinx-hoverxref``
* ``pip install sphinxcontrib-video``

Config file:
-------------
* Sửa file "conf.py"
    * ``html_theme = 'sphinx_rtd_theme'``

Hướng dẫn buid trên readthedoc.org
=====================================

Khai báo file ``.readthedocs.yaml``::

    # .readthedocs.yaml
    # Read the Docs configuration file
    # See https://docs.readthedocs.io/en/stable/config-file/v2.html for details

    # Required
    version: 2

    # Set the OS, Python version and other tools you might need
    build:
      os: ubuntu-22.04
      tools:
        python: "3.12"
        # You can also specify other tool versions:
        # nodejs: "19"
        # rust: "1.64"
        # golang: "1.19"

      jobs: #kxn fix bub build OK
        post_create_environment:
          - python -m pip install sphinx_rtd_theme

    # Build documentation in the "docs/" directory with Sphinx
    sphinx:
      configuration: conf.py

    # Optionally build your docs in additional formats such as PDF and ePub
    # formats:
    #    - pdf
    #    - epub

    # Optional but recommended, declare the Python requirements required
    # to build your documentation
    # See https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html
    # python:
    #    install:
    #    - requirements: docs/requirements.txt

