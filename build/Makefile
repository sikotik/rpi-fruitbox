CPP         = g++
CFLAGS      = -O2 -std=c++14
DEPS        = fruitbox.hpp fruitbox_types.hpp pages.hpp status.hpp playqueue.hpp audio.hpp config.hpp config_base.hpp database.hpp display.hpp \
              engine.hpp fruitbox_logo.hpp info_bkgnd.hpp chooser_arrow.hpp info_font.hpp status_events.hpp userguide.hpp bitmap.hpp joystick.hpp display_base.hpp input.hpp
OBJ         = fruitbox.o playqueue.o audio.o config.o database.o display.o engine.o pages.o status.o userguide.o bitmap.o joystick.o input.o
LIBS        = -lmpg123 -lm -ldl -lallegro -lallegro_memfile -lallegro_font -lallegro_ttf -lallegro_primitives -lallegro_image -lallegro_audio -lallegro_acodec -lallegro_video -lpthread

%.o: %.cpp $(DEPS)
	$(CPP) -c -o $@ $< $(CFLAGS) 

# ./fruitbox: $(OBJ)
./fruitbox: $(OBJ)
	$(CPP) -Wall -o $@ $^ $(CFLAGS) $(LIBS) `pkg-config --libs `

.PHONY: clean
clean:
	rm -f *.o
	rm -f ./fruitbox
	touch Makefile
	touch *.?pp
