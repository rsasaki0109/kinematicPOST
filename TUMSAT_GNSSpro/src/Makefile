CXX = g++

CXXFLAGS = -O2 -std=c++11 -Wno-unused-variable

TARGET = kinematicPOST

SRC_CPP = $(wildcard *.cpp)
SRC_C = $(wildcard *.c)

OBJ = $(SRC_CPP:.cpp=.o) $(SRC_C:.c=.o)

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CXX) $(CXXFLAGS) -o $@ $^

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $<

clean:
	rm -f $(OBJ) $(TARGET)