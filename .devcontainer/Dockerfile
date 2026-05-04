FROM espressif/idf:latest

RUN apt-get update && apt-get install -y --no-install-recommends \
    vim tree minicom usbutils python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --no-cache-dir --break-system-packages \
    pandas matplotlib numpy pyserial esptool rich

RUN mkdir -p /commandhistory && \
    echo 'export HISTFILE=/commandhistory/.bash_history' >> /root/.bashrc

RUN echo '. /opt/esp/idf/export.sh' > /etc/profile.d/esp-idf.sh

WORKDIR /workspace
