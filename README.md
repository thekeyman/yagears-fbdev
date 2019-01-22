# Yet Another Gears OpenGL demo #
A conversion of the popular gears OpenGL demo to the Mali OpenGL ES fbdev

# Compiling

The following libraries must be installed:

	sudo apt-get install pkg-config libpng-dev zlib1g-dev

Assuming libMali.so is in path "/opt/libmali-fbdev-r5p0", type:

	autoreconf -fvi
	export GLESV2_CFLAGS="-DGLESV2_H=\<GLES2/gl2.h\>"
	export EGL_LIBS="-L/opt/libmali-fbdev-r5p0 -lEGL -lGLESv2"
	export EGL_CFLAGS="-I./3rdparty/gles_headers/fbdev"
	./configure --disable-glesv1_cm
	make
  
 # Running
 Your user must have permision to access /dev/mali.
 
 Type:
 
 	./yagears-fbdev -b egl-fbdev -e glesv2
  
