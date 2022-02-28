build:
	go build

run:
	./awesome-api >./awesome.log 2>&1 &

stop:
	kill $$(pgrep -f "awesome-api") > /dev/null 2>&1 &

clean: 
	rm -rf ./awesome-api ./awesome.log > /dev/null 2>&1

test: 
	curl http://localhost:9999
        curl http://localhost:9999/health

help:
	grep '##' ./Makefile | sed 's/ ##/ /' | head -n -1
