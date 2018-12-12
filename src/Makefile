build:
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o benchmark.o benchmark.cpp
	/usr/lib64/openmpi/bin/mpicc -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o main.o main.cpp
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o position.o position.cpp
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o search.o search.cpp
	/usr/lib64/openmpi/bin/mpicc -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o thread.o thread.cpp
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o timeman.o timeman.cpp
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o tt.o tt.cpp
	/usr/lib64/openmpi/bin/mpicc -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o uci.o uci.cpp
	g++ -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto   -c -o ucioption.o ucioption.cpp
	/usr/lib64/openmpi/bin/mpic++ -o stockfish benchmark.o bitbase.o bitboard.o endgame.o evaluate.o main.o material.o misc.o movegen.o movepick.o pawns.o position.o psqt.o search.o thread.o timeman.o tt.o uci.o ucioption.o syzygy/tbprobe.o  -m64 -Wl,--no-as-needed -lpthread -Wall -Wcast-qual -fno-exceptions -std=c++11  -pedantic -Wextra -Wshadow -m64 -DNDEBUG -O3 -DIS_64BIT -msse -flto
