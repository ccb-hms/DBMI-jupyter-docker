FROM python:3.11.4

# Set the working directory in the container
RUN mkdir dbmi-docker

WORKDIR /dbmi-docker

COPY Code/. /Code/.
COPY Container/. /Container/.
COPY Data/. /Data/.

RUN python3 -m pip install jupyterlab
RUN python3 -m pip install langchain
RUN python3 -m pip install langchain-openai
RUN python3 -m pip install langchain-core
RUN python3 -m pip install langchain-community
RUN python3 -m pip install faiss-cpu

EXPOSE 8787

CMD jupyter-lab /Code/dbmi-demo.ipynb --ip 0.0.0.0 --port 8787 --allow-root


# Docker build command:
# docker build . -f Container/Dockerfile -t dbmi-jupyter-workbench

# Docker run command:
# docker \
# run \
# -p 8787:8787 \
# -v ./:/dbmi-docker/ \
# dbmi-jupyter-workbench
