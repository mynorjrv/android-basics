# Setting up Android Studio

I actually already tried this xd `Bitacora.md` have all my previous notes on installing AS. 

The problem I found before was that the VM I set up didnt have enough space. I am setting one with more space and I will try to run it again.

Meanwhile, there are some interesting commands to check the computer specifications in the course codelab.

- `lscpu` to check cpu info
- `free -m` to check total memory
- `df -h` to check disk space
- `xrandr | grep '*'` to check screen resolution

What comes next is basically whay I did in `Bitacora.md` so I will not write it here.

Actually, there is another interesting command. They decrompress the tar.gz with 

```Bash
tar -xzvf android-studio-2022.2.1.20-linux.tar.gz
```

instead of `-xf` which I originally used. I will use mine jeje

Installing this time was super fast, hopefully I have enough disk space to run the emulator now.

# First Android App

Just following the tutorial.

- Created a new Empty Activity project.
- Named the project.
- Wait until dependencies were installed.
- While waiting, closed the Whats new? window.
- Changed to split view to see the code and the preview.
- Preview was empty so pressed Build & Refresh, waited a bit and now I can see Hello Android!

Uhhhhh in the files explorer I can select "views". The default is Android which shows an app directory with a kotlin+java directory with some directories with com.example.greetingcard name, which is the one selected when creating the project.

The "view" can be changed to see the structure of the project as in a file explorer. The "view" to do this is Project Source Files.

And that is not begginer friendly wtf xd

The code is not exactly the same as in the tutorial, so immmm gonna continue tomorrow. 
