# LLM Experiments

This repo is some code and experiments based on "LLM From Scratch" described
in https://github.com/angelos-p. I built/copied that code, and we'll see
what happens next.

## Setup

```
uv sync
```
That will take a while installing about 750 MB of dependencies.

## Training

To train a little model:
```
python src/train.py --data_path data/shakespeare.txt --layers 2 --heads 2 --embeds 128
```

That will create a series of checkpoint files, the last of which is
`checkpoint-2-2-128_final.pt`.

## Generating text

To generate some text from that checkpoint and the prompt "To be or not":

```
python src/generate.py checkpoint-2-2-128_final.pt
```
