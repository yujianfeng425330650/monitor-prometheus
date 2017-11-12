FROM        quay.io/prometheus/busybox:glibc
MAINTAINER  The Prometheus Authors <prometheus-developers@googlegroups.com>

COPY node_exporter /bin/node_exporter

EXPOSE      9100
USER        nobody
ENTRYPOINT  [ "/bin/node_exporter" ]
CMD ["--path.procfs","/host/proc","--path.sysfs","/host/sys","--collector.filesystem.ignored-mount-points"," ^/(sys|proc|dev|host|etc)($|/)"]
