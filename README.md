# Kubeflow + Python + Ollama

This is a Docker image containing a VSCode server, Python and Ollama.
It is meant to be deployed in Kubeflow as a Jupyter notebook server.
You can use this image as is, or as a base image for your own custom images.

The default user is `jovyan` with UID `1001`, which is the default user in Kubeflow. The mount path for new volumes is `/home/jovyan`.

Sudo is enabled and allowed by default in this image.

There is a new empty `.venv` folder by default in `/home/jovyan` that you can use for your Python virtual environment.

## Getting Started

When connected to the container's VSCode server, run `ollama serve` in the terminal to start Ollama. This is a blocking command, meaning you will need to open a secondary terminal to run other commands.

You can activate the Python virtual environment using `source .venv/bin/activate`.
