FROM docker.io/clickable/amd64-20.04-arm64
LABEL base_image_hash="sha256:c5344d6c637a161538d587918b230e4d91e867ef6790c18de086617a5c27de37"
ARG GOPATH="/home/anmol-garg/.clickable/go"
ARG SDK_FRAMEWORK="ubuntu-sdk-20.04.1"
ARG CLICK_FRAMEWORK="ubuntu-sdk-20.04.1"
ARG CLICK_FRAMEWORK_BASE="20.04"
ARG APPARMOR_POLICY="20.04"
ARG QT_VERSION="5.12"
ARG ARCH="arm64"
ARG ARCH_TRIPLET="aarch64-linux-gnu"
ARG ARCH_RUST="aarch64-unknown-linux-gnu"
ARG NUM_PROCS="16"
ARG ROOT="/home/anmol-garg/tmm-fork/timemanagement"
ARG BUILD_DIR="/home/anmol-garg/tmm-fork/timemanagement/build/aarch64-linux-gnu/app"
ARG SRC_DIR="/home/anmol-garg/tmm-fork/timemanagement"
ARG INSTALL_DIR="/home/anmol-garg/tmm-fork/timemanagement/build/aarch64-linux-gnu/app/install"
ARG CLICK_LD_LIBRARY_PATH="/home/anmol-garg/tmm-fork/timemanagement/build/aarch64-linux-gnu/app/install/lib/aarch64-linux-gnu"
ARG CLICK_PATH="/home/anmol-garg/tmm-fork/timemanagement/build/aarch64-linux-gnu/app/install/lib/aarch64-linux-gnu/bin"
ARG CLICK_QML2_IMPORT_PATH="/home/anmol-garg/tmm-fork/timemanagement/build/aarch64-linux-gnu/app/install/lib/aarch64-linux-gnu"

RUN echo set debconf/frontend Noninteractive | debconf-communicate && echo set debconf/priority critical | debconf-communicate
RUN apt-get update && apt-get install -y --force-yes --no-install-recommends python3-pip libatomic1:arm64 && apt-get clean