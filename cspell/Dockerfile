FROM node:20-alpine

ARG CSPELL_VERSION=8.19.4

SHELL ["/bin/sh","-o","pipefail","-c"]

# Install cspell globally
RUN npm install -g cspell@${CSPELL_VERSION} --no-audit --no-fund && npm cache clean --force

# Set working directory
WORKDIR /app

# Copy cspell configuration
COPY cspell.json ./
COPY custom-dict.txt ./



# Download common language dictionaries
RUN cspell link add @cspell/dict-en_us
RUN cspell link add @cspell/dict-en_gb
RUN cspell link add @cspell/dict-companies
RUN cspell link add @cspell/dict-software-terms
RUN cspell link add @cspell/dict-misc
RUN cspell link add @cspell/dict-filetypes
RUN cspell link add @cspell/dict-python
RUN cspell link add @cspell/dict-ar
RUN cspell link add @cspell/dict-az
RUN cspell link add @cspell/dict-be
RUN cspell link add @cspell/dict-bg
RUN cspell link add @cspell/dict-bs
RUN cspell link add @cspell/dict-ca
RUN cspell link add @cspell/dict-cs
RUN cspell link add @cspell/dict-da
RUN cspell link add @cspell/dict-de
RUN cspell link add @cspell/dict-el
RUN cspell link add @cspell/dict-es
RUN cspell link add @cspell/dict-et
RUN cspell link add @cspell/dict-fa
RUN cspell link add @cspell/dict-fi
RUN cspell link add @cspell/dict-fil
RUN cspell link add @cspell/dict-fo
RUN cspell link add @cspell/dict-fr
RUN cspell link add @cspell/dict-fy
RUN cspell link add @cspell/dict-he
RUN cspell link add @cspell/dict-hi
RUN cspell link add @cspell/dict-hr
RUN cspell link add @cspell/dict-ht
RUN cspell link add @cspell/dict-hu
RUN cspell link add @cspell/dict-hy
RUN cspell link add @cspell/dict-id
RUN cspell link add @cspell/dict-is
RUN cspell link add @cspell/dict-it
RUN cspell link add @cspell/dict-ja
RUN cspell link add @cspell/dict-ka
RUN cspell link add @cspell/dict-kk
RUN cspell link add @cspell/dict-kl
RUN cspell link add @cspell/dict-km
RUN cspell link add @cspell/dict-ko
RUN cspell link add @cspell/dict-lb
RUN cspell link add @cspell/dict-lo
RUN cspell link add @cspell/dict-lt
RUN cspell link add @cspell/dict-lv
RUN cspell link add @cspell/dict-mk
RUN cspell link add @cspell/dict-mn
RUN cspell link add @cspell/dict-ms
RUN cspell link add @cspell/dict-mt
RUN cspell link add @cspell/dict-nl
RUN cspell link add @cspell/dict-no
RUN cspell link add @cspell/dict-pl
RUN cspell link add @cspell/dict-ps
RUN cspell link add @cspell/dict-pt
RUN cspell link add @cspell/dict-ro
RUN cspell link add @cspell/dict-ru
RUN cspell link add @cspell/dict-si
RUN cspell link add @cspell/dict-sk
RUN cspell link add @cspell/dict-sl
RUN cspell link add @cspell/dict-sq
RUN cspell link add @cspell/dict-sr
RUN cspell link add @cspell/dict-sv
RUN cspell link add @cspell/dict-sw
RUN cspell link add @cspell/dict-ta
RUN cspell link add @cspell/dict-tg
RUN cspell link add @cspell/dict-th
RUN cspell link add @cspell/dict-tk
RUN cspell link add @cspell/dict-to
RUN cspell link add @cspell/dict-tr
RUN cspell link add @cspell/dict-uk
RUN cspell link add @cspell/dict-ur
RUN cspell link add @cspell/dict-uz
RUN cspell link add @cspell/dict-vi
RUN cspell link add @cspell/dict-zh-cn
RUN cspell link add @cspell/dict-zh-tw
RUN cspell link add @cspell/dict-companies
RUN cspell link add @cspell/dict-django
RUN cspell link add @cspell/dict-dotnet
RUN cspell link add @cspell/dict-fullstack
RUN cspell link add @cspell/dict-golang
RUN cspell link add @cspell/dict-html-symbol-entities
RUN cspell link add @cspell/dict-latex
RUN cspell link add @cspell/dict-lua
RUN cspell link add @cspell/dict-fonts
RUN cspell link add @cspell/dict-k8s
RUN cspell link add @cspell/dict-terraform
# Default command
ENTRYPOINT ["cspell"]
CMD ["--help"]
