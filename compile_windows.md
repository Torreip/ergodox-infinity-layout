This is what I use to launch the compilation with my setup:
    cd docker
    docker build -t ergodox-compile .
    cd ..
    docker run --rm -it -v //f/Documents/_Prog/Github/ergodox-infinity-layout/kiibohd:/kiibohd ergodox-compile ergodox_custom.bash