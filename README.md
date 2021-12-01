# React Intro

## Usage

```sh
# Build
% docker build --no-cache \
    --tag yoshimits_egashira/react-intro \
    --file ./docker/Dockerfile .

# Run container
% docker run --publish 8080:8080 \
    --rm --interactive --tty \
    --name react-intro \
   yoshimits_egashira/react-intro
```