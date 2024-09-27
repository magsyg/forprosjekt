FROM ubuntu:22.04

RUN apt-get update
RUN apt-get install -y python3-pip git wget lshw dmidecode sudo
RUN ulimit -n 65536

RUN mkdir /benchmarks
WORKDIR /benchmarks
COPY . /benchmarks
RUN mkdir /dev/mem

RUN pip3 install click pyyaml tabulate pandas

RUN python3 benchpress_cli.py install video_transcode_bench_svt