FROM alpine:3.12.1
USER root

COPY frpc /root/frp/frpc
RUN  chmod 755 /root/frp/frpc

COPY frpc.ini /root/frp/frpc.ini

WORKDIR /root/frp/

CMD ./frpc -c ./frpc.ini
