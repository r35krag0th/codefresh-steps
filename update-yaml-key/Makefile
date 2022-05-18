.PHONY: all

all: clean
	npx @adobe/jsonschema2md -d schemas -o ./docs

clean:
	rm -f ./docs/*
	rm -rf ./out
