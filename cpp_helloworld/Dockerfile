# Stage 1: Build
# Base Image 1.25GB
FROM rikorose/gcc-cmake as builder
RUN mkdir -p cpp_example/build
COPY CMakeLists.txt hello_world_cmake.cpp cpp_example/
WORKDIR cpp_example/build
RUN cmake ..
RUN make
RUN ./hello_world_cmake

# Stage 2: Run
# Base Image 120MB
FROM ubuntu:16.04
COPY --from=builder /cpp_example/build/hello_world_cmake /hello_world_cmake
CMD ["./hello_world_cmake"]
