FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    cmake \
    ninja-build \
    python3 \
    python3-pip \
    curl \
    wget \
    unzip \
    libusb-1.0-0-dev \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install -y \
    gcc-arm-none-eabi \
    gdb-multiarch \
    openocd \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /stm32_ws
WORKDIR /stm32_ws

RUN pip3 install --no-cache-dir \
    pyserial \
    click 

CMD ["/bin/bash"]