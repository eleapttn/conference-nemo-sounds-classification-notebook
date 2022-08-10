# Nemo notebook

Notebook for data processind and AI model training.

## Data

```console
├── data
    └── marine-mammal-sound-test1.wav
    └── data.csv
    └── ai-model
```

## Launch it with AI Notebooks 

```console
ovhai notebook run one-for-all jupyterlab \
	--name nemo-notebook \
	--gpu 1 \
	--volume nemo-data@GRA/:/workspace/data:RW:cache
```
