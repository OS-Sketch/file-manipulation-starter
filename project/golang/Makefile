all: copy

clean:
	rm -f bin/copy

bin:
	mkdir bin

copy: copy.go bin
	go build --o bin copy.go
