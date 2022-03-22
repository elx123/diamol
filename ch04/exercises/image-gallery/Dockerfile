FROM diamol/golang As test1
COPY main.go .
RUN go build -o /server

FROM diamol/base
WORKDIR /web
COPY --from=test1 /server .
RUN chmod +x server
CMD [ "/web/server" ]

