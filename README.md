# twherohan



Text generation system based on a mixed corpus of [韓國瑜 facebook](https://www.facebook.com/twherohan/)

## form
https://github.com/pyliaorachel/resurrecting-the-dead-chinese
## Usage

###### Mix corpus

```bash
$ cd src/corpus
$ python3 mix.py <first-corpus> <second-corpus> --output <output-corpus-text-file>

# Or directly run
$ ./run.sh
```

###### Train

```bash
$ cd src
$ python3 -m train.train <corpus-text-file> 

# For more options
$ python3 -m train.train -h

# Or directly run
$ ./train.sh
```

Outputs:

- `model.bin`: torch model
- `corpus.bin`: parsed corpus, mapping, & vocabulary

###### Text generation

```bash
$ cd src
$ python3 -m generate_text.gen <corpus-bin-file> <model-bin-file>

# For more options
$ python3 -m generate_text.gen -h

# Or directly run
$ ./gen.sh
```
