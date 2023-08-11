CC = gcc
CFLAGS = -Wall -g
OBJS =  main.o operations.o admin.o user.o
TARGET = stack

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $(TARGET)

operation.o : operations/operations.c operations/operations.h 
	$(CC) $(CFLAGS) -c operations/operations.c

admin.o : adminAnduser/admin.c adminAnduser/user.h 
	$(CC) $(CFLAGS) -c adminAnduser/admin.c

user.o : adminAnduser/user.c adminAnduser/user.h 
	$(CC) $(CFLAGS) -c adminAnduser/user.c

main.o: main.c stack.h
	$(CC) $(CFLAGS) -c main.c

clean:
	rm -f $(OBJS) $(TARGET)