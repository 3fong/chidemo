FROM alpine:latest
RUN /bin/sed -i 's,http://dl-cdn.alpinelinux.org,https://mirrors.aliyun.com,g' /etc/apk/repositories
RUN apk update && apk add ca-certificates && rm -rf /var/cache/apk/*
COPY /opt/workspace/go/chidemo/chi .
EXPOSE 8084
ENTRYPOINT [ "./chi" ]
