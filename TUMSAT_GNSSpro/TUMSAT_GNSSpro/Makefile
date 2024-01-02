CXX = g++

CXXFLAGS = -O2 -std=c++11 -Wno-unused-variable -g

TARGET = ../Debug/kinematicPOST

SRC_DIR = ../src
BUILD_DIR = ../Debug

SRC_CPP = $(wildcard $(SRC_DIR)/*.cpp)
SRC_C = $(wildcard $(SRC_DIR)/*.c)

OBJ = $(SRC_CPP:$(SRC_DIR)/%.cpp=$(BUILD_DIR)/%.o) $(SRC_C:$(SRC_DIR)/%.c=$(BUILD_DIR)/%.o)

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CXX) $(CXXFLAGS) -o $@ $^

$(BUILD_DIR)/%.o: $(SRC_DIR)/%.cpp
	mkdir -p $(BUILD_DIR)
	$(CXX) $(CXXFLAGS) -c $< -o $@

$(BUILD_DIR)/%.o: $(SRC_DIR)/%.c
	mkdir -p $(BUILD_DIR)
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ) $(TARGET)
