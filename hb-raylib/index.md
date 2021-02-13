---
title: "hb-raylib"
---

# **Harbour project extended xBase compiler.**

![Logo](assets/img/harbour_raylib.svg)

**hb-raylib** is a cross-platform open-source software development library. The library is meant to create graphical applications and games. The source code is written in C Language. It supports compilation to many target platforms, including Windows, GNU Linux, macOS, FreeBSD, Android.

View the project on [GitHub](https://github.com/rjopek/hb-raylib)

> - [module: core](core "module: core")
> - [module: shapes](shapes "module: shapes")
> - [module: textures](textures "module: textures")
> - [module: text](text "module: text")
> - [module: models](models "module: models")
> - [module: shaders (rlgl)](shaders_rlgl "module: shaders (rlgl)")
> - [module: audio](audio "module: audio")
> - [structs](structs "structs")
> - [colors](colors "colors")

### Example code

{% highlight ruby %}
#include "hbraylib.ch"

PROCEDURE Main()

   LOCAL nScreenWidth := 800
   LOCAL nScreenHeight := 450

   InitWindow( nScreenWidth, nScreenHeight, "Harbour and raylib [core] example - basic window" )

   SetTargetFPS( 60 )

   DO WHILE ! WindowShouldClose()

      BeginDrawing()

         ClearBackground( RAYWHITE )

         DrawText( "Congrats! You created your first window!", 190, 200, 20, LIGHTGRAY )

      EndDrawing()

   ENDDO

   CloseWindow()

   RETURN
{% endhighlight %}

![](docs/assets/img/core_basic_window.png)

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](.git/LICENSE)

Licencja MIT is obviously applied only for this repository, not what it builds.

<br>
<br>
<br>

> &copy; 2020 Rafał Jopek
