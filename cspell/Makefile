.PHONY: help check fix docker-build docker-check

help:
	@echo "Available commands:"
	@echo "  check        - Run spell check on all files"
	@echo "  fix          - Auto-fix spelling issues where possible"
	@echo "  docker-build - Build Docker image for spell checking"
	@echo "  docker-check - Run spell check using Docker"

check:
	cspell --config cspell.json "**/*"

fix:
	cspell --config cspell.json "**/*" --fix

docker-build:
	docker build -t holidays-cspell .

docker-check:
	docker run --rm -v $(PWD)/../:/app holidays-cspell cspell "**/*"
