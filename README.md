# FAISS CPU Docker Workbench

A dockerized Jupyter notebook for completing AI tasks with faiss, openai, and lang chain.

## Building the image
```
docker build . -f Container/Dockerfile -t faiss-cpu-docker-workbench
```

## Running the image

```
docker \
run \
-p 8787:8787 \
-v ./:/faiss-cpu-docker-workbench/ \
faiss-cpu-docker-workbench
```

If you're using windows you may need to give the command as a single line:

```
docker run -p 8787:8787 -v ./:/faiss-cpu-docker-workbench/ faiss-cpu-docker-workbench
```

## Connecting to the container/jupyter notebook

Upon running, your terminal will display a link to the web address of your running jupyter notebook. Copy this link into your browser to begin testing.
