Set Up Steps:

1. Install Dev C++: If you haven't already, download and install Dev C++ from the official website: https://sourceforge.net/projects/orwelldevcpp/. ( Tested version 5.11 )

2. Download Graphics Library: Download required files from this repository.

3. Move Files: Move the downloaded graphics.h and winbgim folder directly to the include folder inside the Dev C++ installation directory. Typically, the path is C:\Dev-Cpp\MinGW64\include.
               and also add libbgi.a to the lib folder.

4. Configure Linker Options: Open Dev C++, go to Tools > Compiler Options. Under the "General" tab, select "Add the followoing commands when calling the linker:".
             " -static-libgcc -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32"  paste this and           Click "OK" to save.

5. Testing: To test if everything is set up correctly, create a new C or C++ file in Dev C++. Write a simple graphics program, for example:

              #include <graphics.h>
              int main() {
              int gd = DETECT, gm;
              initgraph(&gd, &gm, "");
              circle(300, 200, 100);
              delay(5000);
              closegraph();
              return 0;
              }


