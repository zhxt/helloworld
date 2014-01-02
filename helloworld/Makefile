CFLAGS := -g -Wall
TARGET := hello
SOURCES := $(shell find src -type f -name *.c)
OBJECTS := $(SOURCES:%.c=%.o)

PREFIX = /usr
BINDIR = $(PREFIX)/bin

all: $(TARGET)

$(TARGET): $(OBJECTS)
	$(CC) $^ -o $(TARGET)

install: all
	@echo "  Installing...";
	install -D $(TARGET) $(DESTDIR)$(BINDIR)/$(TARGET)

clean:
	@echo "  Cleaning..."; $(RM) -r $(OBJECTS) $(TARGET)

.PHONY: all install uninstall clean
