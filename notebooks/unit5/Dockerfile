FROM python:3.10.12-slim-bookworm AS unity-base
ENV PYTHONUNBUFFERED=1 PIP_NO_CACHE_DIR=1
RUN apt-get update && apt-get install -y --no-install-recommends libglib2.0-0 libgl1 libx11-6 libxcursor1 libxrandr2 libxinerama1 libxi6 libasound2 libnss3 ca-certificates && rm -rf /var/lib/apt/lists/*
FROM unity-base
RUN python -m pip install --upgrade 'pip<25' 'setuptools<70' wheel && python -m pip install 'torch==2.5.1' --index-url https://download.pytorch.org/whl/cu124
RUN python -m pip install 'mlagents==1.1.0' 'huggingface-hub<1' 'protobuf==3.20.3'
WORKDIR /work
