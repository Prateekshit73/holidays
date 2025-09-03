FROM node:20-alpine

# Install cspell globally
RUN npm install -g cspell@latest

# Set working directory
WORKDIR /app

# Copy cspell configuration
COPY cspell.json ./
COPY custom-dict.txt ./

# Create dictionaries directory
RUN mkdir -p dictionaries

# Download common language dictionaries
RUN cspell link add @cspell/dict-en_us
RUN cspell link add @cspell/dict-en_gb
RUN cspell link add @cspell/dict-companies
RUN cspell link add @cspell/dict-software-terms
RUN cspell link add @cspell/dict-misc
RUN cspell link add @cspell/dict-filetypes
RUN cspell link add @cspell/dict-python

# Default command
CMD ["cspell", "--help"]
