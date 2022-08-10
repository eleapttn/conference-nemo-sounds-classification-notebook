# Nemo notebook - marine mammal sounds classification

*Notebook to build and train an audio classifier.*

## Data

In this tuorial, we will use the first 45 marine mammals of this [dataset](https://cis.whoi.edu/science/B/whalesounds/index.cfm).

Upload your data in an OVHCloud Object Storage container:

```console
ovhai data upload gra nemo-data data.csv marine-mammal-sound-test1.wav
```

Your data should be as follow:

```console
├── data
    └── marine-mammal-sound-test1.wav
    └── data.csv
```

## AI Notebook

Launch an OVHcloud AI Notebook to buid and train your model!

```console
ovhai notebook run one-for-all jupyterlab \
	--name nemo-notebook \
	--gpu 1 \
	--volume nemo-data@GRA/:/workspace/data:RW:cache
```

At the end of your training, your Object Storage container sould be like that:

```console
├── data
    └── marine-mammal-sound-test1.wav
    └── data.csv
    └── ai-model
```

## References

If you want to run all the tutorial from scratch, please refer to:

- The full notebook [here](https://github.com/ovh/ai-training-examples/blob/main/notebooks/audio/audio-classification/notebook-marine-sound-classification.ipynb)
- The documentation on this [link](https://docs.ovh.com/gb/en/publiccloud/ai/notebooks/tuto-marine-mammal-sounds-classification/)
