FROM alpine:3.12.1
USER root

COPY frps /root/frp/frps
RUN  chmod 755 /root/frp/frps

COPY frps.ini /root/frp/frps.ini

WORKDIR /root/frp/

# 中繼端口
EXPOSE 8002
EXPOSE 8003
EXPOSE 33389

CMD ./frps -c ./frps.ini
