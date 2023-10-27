# Ubuntu 22.04
FROM ubuntu:jammy

RUN apt -y update
RUN apt -y install git gcc make

RUN git clone https://github.com/Lora-net/sx1302_hal.git /sx1302_hal
RUN make --directory=/sx1302_hal

# run on container startup
CMD /sx1302_hal/packet_forwarder/lora_pkt_fwd -c /sx1302_hal/packet_forwarder/global_conf.json
