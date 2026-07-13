# Word2Vec

To create a docker image
``` cmd
git clone <repo link>
cd <this folder>
docker build . -t nlp
```

To run the container and launch the ipynb file
``` cmd
docker run -it --gpus=all -v "%cd%":/workspace/code -p 8888:8888 nlp bash
cd code
jupyter notebook --ip 0.0.0.0 --allow-root --NotebookApp.token='' --NotebookApp.password='' --ServerApp.iopub_msg_rate_limit=10000000.0
```
