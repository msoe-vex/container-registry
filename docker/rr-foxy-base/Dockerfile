FROM ros:foxy-ros-base-focal

RUN sudo apt-get update && \
    sudo apt-get install -y software-properties-common && \
    sudo apt-get update && \
    sudo add-apt-repository -y ppa:git-core/ppa && \
    sudo apt-get update && \
    sudo apt-get install -y git python3 python3-pip python-is-python3 python3-rosdep libeigen3-dev wget && \
    sudo apt-get update && \
    sudo mkdir /install-dir && \
    cd /install-dir && \
    wget https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/9-2020q2/gcc-arm-none-eabi-9-2020-q2-update-x86_64-linux.tar.bz2 --no-check-certificate && \
    tar -xjvf gcc-arm-none-eabi-9-2020-q2-update-x86_64-linux.tar.bz2 && \
    sudo python -m pip install https://github.com/purduesigbots/pros-cli/releases/download/3.1.4/pros_cli_v5-3.1.4-py3-none-any.whl

ENV PATH "$PATH:/install-dir/gcc-arm-none-eabi-9-2020-q2-update/bin/"

RUN echo "export PATH=/install-dir/gcc-arm-none-eabi-9-2020-q2-update/bin/:${PATH}" >> /root/.bashrc

RUN echo "source /opt/ros/foxy/setup.bash" >> /root/.bashrc