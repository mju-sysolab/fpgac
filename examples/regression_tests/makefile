tests: loops4 loops7 loops8 loops9 ioports1 regression

clean:
	rm -f *.cnf *.xnf *.ucf test.c

loops4: loops_4_for.c loops_4_while.c
	cp loops_4_for.c   test.c; fpgac -target cnf test.c; mv test.cnf loops_4_for.cnf
	cp loops_4_while.c test.c; fpgac -target cnf test.c; mv test.cnf loops_4_while.cnf
	rm -f test.c
	-diff loops_4*.cnf

loops7: loops_7_for.c loops_7_while.c
	cp loops_7_for.c   test.c; fpgac -target cnf test.c; mv test.cnf loops_7_for.cnf
	cp loops_7_while.c test.c; fpgac -target cnf test.c; mv test.cnf loops_7_while.cnf
	rm -f test.c
	-diff loops_7*.cnf

loops8: loops_8_for.c loops_8_while.c
	cp loops_8_for.c   test.c; fpgac -target cnf test.c; mv test.cnf loops_8_for.cnf
	cp loops_8_while.c test.c; fpgac -target cnf test.c; mv test.cnf loops_8_while.cnf
	rm -f test.c
	-diff loops_8*.cnf

loops9: loops_9_for.c loops_9_while.c
	cp loops_9_for.c   test.c; fpgac -target cnf test.c; mv test.cnf loops_9_for.cnf
	cp loops_9_while.c test.c; fpgac -target cnf test.c; mv test.cnf loops_9_while.cnf
	rm -f test.c
	-diff loops_9*.cnf

ioports1: ioports_1.c
	-fpgac -target cnf ioports_1.c

regression:
	-diff loops_4_for.cnf loops_4_for.cnf.orig
	-diff loops_4_while.cnf loops_4_while.cnf.orig
	-diff loops_7_for.cnf loops_7_for.cnf.orig
	-diff loops_7_while.cnf loops_7_while.cnf.orig
	-diff loops_8_for.cnf loops_8_for.cnf.orig
	-diff loops_8_while.cnf loops_8_while.cnf.orig
	-diff loops_9_for.cnf loops_9_for.cnf.orig
	-diff loops_9_while.cnf loops_9_while.cnf.orig
	-diff ioports_1.cnf ioports_1.cnf.orig


orig:  tests
	mv loops_4_for.cnf loops_4_for.cnf.orig
	mv loops_4_while.cnf loops_4_while.cnf.orig
	mv loops_7_for.cnf loops_7_for.cnf.orig
	mv loops_7_while.cnf loops_7_while.cnf.orig
	mv loops_8_for.cnf loops_8_for.cnf.orig
	mv loops_8_while.cnf loops_8_while.cnf.orig
	mv loops_9_for.cnf loops_9_for.cnf.orig
	mv loops_9_while.cnf loops_9_while.cnf.orig
	mv ioports_1.cnf ioports_1.cnf.orig
