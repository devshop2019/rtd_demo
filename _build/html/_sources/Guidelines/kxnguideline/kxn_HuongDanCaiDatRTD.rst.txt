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

Config file:
-------------
* Sửa file "conf.py"
    * ``html_theme = 'sphinx_rtd_theme'``