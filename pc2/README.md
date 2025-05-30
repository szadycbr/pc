# PCjs Emulator for Wolfenstein 3D (User-Provided Image)

This directory contains a self-contained PCjs emulator setup configured for a Compaq DeskPro 386 with a VGA display. It has been modified from the original pcjs.org Wolfenstein 3D page to allow users to load their own floppy disk images (e.g., a Wolfenstein 3D `.img` file).

## How to Use

1.  **Host these files:** The contents of this `pc2` directory (including `index.html`, the `assets` directory, and the `machines` directory) need to be hosted on a web server. You cannot simply open the `index.html` file directly in your browser from your local filesystem due to browser security restrictions (CORS issues related to loading XML and other resources).
    *   A simple way to do this locally is to use Python's built-in HTTP server. Open a terminal or command prompt in this `pc2` directory and run:
        *   If you have Python 3: `python -m http.server`
        *   If you have Python 2: `python -m SimpleHTTPServer`
    *   Then, open your web browser and go to `http://localhost:8000` (or whatever port the server indicates).

2.  **Load your disk image:**
    *   Once the `index.html` page is loaded in your browser, you should see the PCjs emulator interface.
    *   Look for "Drive A (1.44MB)" (or a similar label for the floppy drive) in the emulator's control panel or menus.
    *   There should be an option to "Load" or "Mount" a disk image. Click this and select your Wolfenstein 3D `.img` or other compatible floppy disk image file from your local computer.

3.  **Run the game:**
    *   After the disk image is loaded into Drive A, the emulator should behave as if a floppy has been inserted.
    *   You may need to type standard DOS commands in the emulator's virtual screen to start the game (e.g., `A:`, then `DIR` to see files, then the name of the game's executable, often `WOLF3D.EXE` or `INSTALL.EXE` first).

## Contents

*   `index.html`: The main page to load the emulator.
*   `assets/`: Contains CSS stylesheets and fonts necessary for PCjs.
*   `machines/`: Contains the PCjs machine definition files (`.xml`), JavaScript for the emulator (`pcx86v3.js`), and related assets.
*   `tools/`: Contains auxiliary JavaScript for PCjs UI elements like the explorer.

This setup is based on files from the [PCjs Project](https://www.pcjs.org) by Jeff Parsons.
