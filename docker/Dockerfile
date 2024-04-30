FROM nvcr.io/nvidia/pytorch:23.10-py3

WORKDIR /workspace/
RUN mkdir /workspace/api
ENV PYTHONPATH /workspace/
COPY requirements.txt /workspace/
COPY api /workspace/api

RUN pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple && \
    pip install --no-cache-dir -r /workspace/requirements.txt && \
    pip install bitsandbytes --upgrade