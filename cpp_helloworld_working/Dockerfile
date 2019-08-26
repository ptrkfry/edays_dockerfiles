FROM gcc:8.2 as builder
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
RUN g++ -o myapp -static hello_world.cpp

FROM alpine:latest
COPY --from=builder /usr/src/myapp/myapp /myapp
CMD ["./myapp"]
