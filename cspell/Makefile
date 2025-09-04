# Resolve repo root regardless of where make is invoked from
MAKEFILE_DIR := $(dir $(abspath $(lastword $(MAKEFILE_LIST))))
REPO_ROOT    := $(abspath $(MAKEFILE_DIR)/..)

.PHONY: help check fix docker-build docker-check

help:
	@echo "Available commands:"
	@echo "  check        - Run spell check on all files"
	@echo "  fix          - Auto-fix spelling issues where possible"
	@echo "  docker-build - Build Docker image for spell checking"
	@echo "  docker-check - Run spell check using Docker"

check:
	npx cspell --config cspell.json "**/*"

fix:
	npx cspell --config cspell.json "**/*" --fix

docker-build:
	docker build -t holidays-cspell .

docker-check:
	docker run --rm -v $(REPO_ROOT):/app -w /app holidays-cspell \
	  cspell --config cspell/cspell.json "**/*"
