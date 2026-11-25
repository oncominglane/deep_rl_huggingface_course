FROM deep-rl-unit5:1.1.0
RUN python -m pip install --no-cache-dir 'sample-factory==2.1.1' 'vizdoom==1.2.4' 'opencv-python==4.11.0.86' 'wandb==0.16.6' 'protobuf==3.20.3' 'numpy==1.23.5' 'pandas<2.2' && python -m pip check
RUN python -m pip install --no-cache-dir imageio-ffmpeg==0.6.0 && ln -s "$(python -c "import imageio_ffmpeg; print(imageio_ffmpeg.get_ffmpeg_exe())")" /usr/local/bin/ffmpeg
WORKDIR /work
