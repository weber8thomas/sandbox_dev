FROM condaforge/mambaforge:latest

# Step 1: Retrieve conda environments

RUN mkdir -p /conda-envs/TEST
COPY workflow/envs/env.yaml /conda-envs/TEST/environment.yaml

RUN mkdir -p /conda-envs/TEST2
COPY workflow/envs/env2.yaml /conda-envs/TEST2/environment.yaml

# Step 2: Generate conda environments

RUN mamba env create --prefix /conda-envs/TEST --file /conda-envs/TEST/environment.yaml && \
    mamba env create --prefix /conda-envs/TEST2 --file /conda-envs/TEST2/environment.yaml && \
    mamba clean --all -y

