
# you may need libva-dev i965-va-driver on intel platform

include Makefile.common

TARGET	= asource-system vsource-desktop filter-rgb2yuv ctrl-sdl \
	  encoder-video ctrl-sdl encoder-audio

all:
	for t in $(TARGET); do make -C $$t || exit 1; done

install:
	-mkdir -p ../../bin/mod
	find . -name '*.$(EXT)' -exec cp -f {} ../../bin/mod \;

clean:
	for t in $(TARGET); do make -C $$t clean; done

