docker build . -t nlp

docker run -it --gpus=all -v "%cd%":/workspace/code -p 8888:8888 nlp bash
cd code
jupyter notebook --ip 0.0.0.0 --allow-root --NotebookApp.token='' --NotebookApp.password='' --ServerApp.iopub_msg_rate_limit=10000000.0

