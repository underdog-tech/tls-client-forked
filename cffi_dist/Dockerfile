FROM ubuntu:20.04

# Update and upgrade repo
RUN apt-get update -y -q && apt-get upgrade -y -q

# Install tools we might need
RUN apt-get install --no-install-recommends -y -q curl build-essential ca-certificates git gcc g++ bash gcc-x86-64-linux-gnu libc6-dev-amd64-cross

# Download Go 1.24.1 for the native architecture and install it to /usr/local/go
RUN curl -s https://dl.google.com/go/go1.24.1.linux-amd64.tar.gz | tar -v -C /usr/local -xz

# Let's people find our Go binaries
ENV PATH $PATH:/usr/local/go/bin
