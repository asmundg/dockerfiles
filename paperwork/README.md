# Paperwork docker image

Run paperwork in a docker container.

Paperwork uses X, so we need to mount the X socket. We also need to
mount a directory containing the actual files:

    docker run --rm --net host -v ~/.Xauthority:/root/.Xauthority -v ~/doc/papers:/root/papers -e DISPLAY asmundg/paperwork
