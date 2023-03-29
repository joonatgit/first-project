CC = gcc
CFLAGS = -W -Wall
TARGET = diary_exe
OBJECTS = memo.o main.o calendar.o

run: all
	$(TARGET)
all : $(TARGET)

$(TARGET) : $(OBJECTS)
	$(CC) $(CFLAGS) -o $@ $^

clean :
	rm *.o diary_exe