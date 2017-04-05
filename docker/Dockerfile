FROM debian:jessie

RUN apt-get update && apt-get install -y --no-install-recommends \
		binutils-arm-none-eabi \
		build-essential \
		ca-certificates \
		cmake \
		ctags \
		dfu-util \
		g++-multilib \
		gcc-arm-none-eabi \
		git \
		libusb-1.0-0-dev \
		libnewlib-arm-none-eabi \
		python3 \
	&& rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/Torreip/ergodox_controller.git controller \
	&& mkdir /kiibohd \
	&& cd controller \
    && cd Keyboards \
    && ./ergodox.bash

VOLUME /kiibohd

COPY ./docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
