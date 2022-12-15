FROM alpine:3.12.1
USER root

COPY frps /root/frp/frps
RUN  chmod 755 /root/frp/frps

COPY frps.ini /root/frp/frps.ini

WORKDIR /root/frp/

# 中繼端口
EXPOSE 8000

# 監控端口, 對應Prometheus
# EXPOSE 50099

CMD ./frps -c ./frps.ini