CXXFLAGS = -Iext/gl3w -std=c++11 -Wall -pedantic -DENABLE_SOUND
LIB = -ldl -lGL -lglfw -lSDL -lSDL_mixer -lpthread -lXinerama -lXxf86vm -lXrandr -lXcursor -lXi -lXext -lX11

BIN=a1
OBJ=$(BIN).o common.o fish.o salmon.o turtle.o world.o

default: build
	
build: $(BIN)

test: build
	./$(BIN)

%.o: src/%.cpp
	g++ -c $(CXXFLAGS) -o $@ $<

$(BIN): $(OBJ)
	g++ -o $@ $(OBJ) $(LIB)

clean:
	- rm -f $(BIN) $(OBJ)
