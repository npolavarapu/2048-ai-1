AI for the [2048 game](http://gabrielecirulli.github.io/2048/). This uses *expectimax optimization*, along with a highly-efficient bitboard representation to search upwards of 10 million moves per second on recent hardware. Heuristics used include bonuses for empty squares and bonuses for placing large values near edges and corners.  

## Building

### Unix/Linux/OS X

Run `make`. Any relatively recent C++ compiler should be able to build the output.

### Windows

You have a few options, depending on what you have installed.

- Pure Cygwin: run `make`. The resulting DLL can *only* be used with Cygwin programs, so
to run the browser control version, you must use the Cygwin Python (not the python.org Python).
- Cygwin with MinGW: run

        CXX=x86_64-w64-mingw32-g++ CXXFLAGS='-static-libstdc++ -static-libgcc -D_WINDLL -D_GNU_SOURCE=1' make

    to build. The resultant DLL can be used with non-Cygwin programs.
- Visual Studio: open a Visual Studio command prompt, `cd` to the 2048-ai directory, and run `make-msvc.bat`.

## Running the command-line version

Run `bin/2048` if you want to see the AI by itself in action.

## Running the browser-control version

Install [Remote Control for Firefox](https://addons.mozilla.org/en-US/firefox/addon/remote-control/).

Open up the [2048 game](http://gabrielecirulli.github.io/2048/) or any compatible clone and start remote control.

Run `2048.py` and watch the game!
