CC		= g++
CFLAGS	= -Ofast -c -std=c++11 -Wextra -Wall
LDFLAGS	= -std=c++11 -Wextra -Wall

INC_DIR	= inc
SRC_DIR	= src
OBJ_DIR	= obj

OBJS	= subtract.o main.o
OBJSD	= ${OBJ_DIR}/subtract.o ${OBJ_DIR}/main.o
EXE		= subtract

vpath %.h ${INC_DIR}
vpath %.cpp ${SRC_DIR}
vpath %.obj ${OBJ_DIR}

$(EXE): $(OBJS)
	$(CC) $(LDFLAGS) -I${INC_DIR} $(OBJSD) -o $(EXE)

subtract.o: subtract.cpp
	$(CC) $(CFLAGS) -I${INC_DIR} ${SRC_DIR}/subtract.cpp -o ${OBJ_DIR}/subtract.o

main.o: main.cpp
	$(CC) $(CFLAGS) -I${INC_DIR} ${SRC_DIR}/main.cpp -o ${OBJ_DIR}/main.o

.PHONY : clean

clean :
	-rm -f $(OBJSD) $(EXE)
