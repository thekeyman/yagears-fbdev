# Yet Another Gears OpenGL demo #
A conversion of the popular gears OpenGL demo to the Mali OpenGL ES fbdev

# Compiling

Assuming libMali.so is in your ld.conf path. e.g.:

	sudo echo "/opt/libmali-fbdev-r5p0" > /etc/ld.so.conf.d/00-mali-fbdev.conf
	sudo ldconfig

Type:

	autoreconf -fvi
	export GLESV2_CFLAGS="-DGLESV2_H=\<GLES2/gl2.h\>"
	export EGL_LIBS="-lEGL -lGLESv2"
	export EGL_CFLAGS="-I./3rdparty/gles_headers/fbdev"
	./configure --disable-glesv1_cm
	make
  
 # Running
 
 	./yagears-fbdev -b egl-fbdev -e glesv2
  
