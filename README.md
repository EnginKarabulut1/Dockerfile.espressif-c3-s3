Zephyr ESP32-C3/ESP32-S3 Development Docker Image
-------------------------------------------------------------

This repository provides a fully-featured Docker image for Zephyr RTOS development on Espressif SoCs, including ESP32-C3(RISC-V), and ESP32-S3(Xtensa).
It includes the Zephyr OS source tree, Zephyr SDK toolchains, Espressif HAL blobs, west tools, VS Code Server, and essential development utilities — all preconfigured and ready to use.

This container is ideal for:

🧪 Embedded development
⚙️ Building and flashing Zephyr applications
💻 Remote development with VS Code Server
🧰 Reproducible builds (frozen Zephyr revision & SDK version)

-------------------------------------------------------------
VS Code Server
with preinstalled extensions:
C/C++ Tools
CMake Tools
Hex Editor
Nordic Devicetree Viewer

🖥️ SSH Support
Includes an SSH server with:
root login enabled
default password: "zephyr"
-------------------------------------------------------------
Build the image (this will take some time):

docker build -t env-zephyr-espressif-c3-s3 -f Dockerfile.espressif-c3-s3 .

Run the image:

docker run -it --rm -v "$(pwd)/workspace:/workspace" -w /workspace -p 2222:22 -p 8800:8800 env-zephyr-espressif-c3-s3



