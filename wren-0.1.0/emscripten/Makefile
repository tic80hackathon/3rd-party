CFLAGS = -DWREN_OPT_META -DWREN_OPT_RANDOM
CC = emcc

FILES = \
	wren_compiler.o \
	wren_core.o \
	wren_debug.o \
	wren_primitive.o \
	wren_utils.o \
	wren_value.o \
	wren_vm.o \
	wren_opt_meta.o \
	wren_opt_random.o

all: libwren.a

libwren.a: $(FILES)
	emar rcu $@ $(FILES)
	emranlib $@

wren_compiler.o: wren_compiler.c
	$(CC) -c wren_compiler.c $(CFLAGS) -o $@

wren_core.o: wren_core.c
	$(CC) -c wren_core.c $(CFLAGS) -o $@

wren_debug.o: wren_debug.c
	$(CC) -c wren_debug.c $(CFLAGS) -o $@

wren_primitive.o: wren_primitive.c
	$(CC) -c wren_primitive.c $(CFLAGS) -o $@

wren_utils.o: wren_utils.c
	$(CC) -c wren_utils.c $(CFLAGS) -o $@

wren_value.o: wren_value.c
	$(CC) -c wren_value.c $(CFLAGS) -o $@

wren_vm.o: wren_vm.c
	$(CC) -c wren_vm.c $(CFLAGS) -o $@

wren_opt_meta.o: wren_opt_meta.c
	$(CC) -c wren_opt_meta.c $(CFLAGS) -o $@

wren_opt_random.o: wren_opt_random.c
	$(CC) -c wren_opt_random.c $(CFLAGS) -o $@

