FROM library/debian:experimental

RUN apt update && apt upgrade -y && apt install -t experimental -y \
	wine \
	--no-install-recommends && \
	dpkg --add-architecture i386 && \
	apt update && \
	apt install -t experimental -y \
	wine32 \
    winetricks \
    wine-development \
    wine64 \
    wine64-development \
    wine64-tools \
    fonts-wine  \
    wine32-tools \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENV HOME /root
WORKDIR $HOME
