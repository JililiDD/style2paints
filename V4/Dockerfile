FROM python:3.6.15
WORKDIR /usr/src/app
COPY ./s2p_v4_server/requirements.txt ./
RUN pip install --no-cache-dir --upgrade pip setuptools wheel \
  && pip install --no-cache-dir -r requirements.txt \
  && pip install --no-cache-dir 'h5py==2.10.0' --force-reinstall
COPY . .
WORKDIR /usr/src/app/s2p_v4_server
CMD ["python", "./server.py"]