all:withdraw_simple withdraw_threaded

withdraw_simple:withdraw_simple.c withdraw_shared.c withdraw_shared.h
	gcc -Wall -Werror withdraw_simple.c withdraw_shared.c -o withdraw_simple

withdraw_threaded:withdraw_threaded.c withdraw_shared.c withdraw_args.c withdraw_args.h withdraw_shared.h withdraw_scoped.h
	g++ -Wall -Werror -pthread withdraw_threaded.c withdraw_shared.c withdraw_args.c -o withdraw_threaded

.PHONY: clean
clean:
	rm withdraw_simple withdraw_threaded
