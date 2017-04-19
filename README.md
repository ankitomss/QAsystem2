# Dynamic memory networks in Theano

## Usage

This implementation is based on Theano and Lasagne. One way to install them is:

    pip install -r https://raw.githubusercontent.com/Lasagne/Lasagne/master/requirements.txt
    pip install https://github.com/Lasagne/Lasagne/archive/master.zip

The following bash scripts will download bAbI tasks and GloVe vectors.

    ./fetch_babi_data.sh
    ./fetch_glove_data.sh

Use `main.py` to train a network:

    python main.py --network dmn_basic --babi_id 1

The states of the network will be saved in `states/` folder. 
There is one pretrained state on the 1st bAbI task. It should give 100% accuracy on the test set:

    python main.py --network dmn_basic --mode test --babi_id 1 --load_state states/dmn_basic.mh5.n40.babi1.epoch4.test0.00033.state

## License
[The MIT License (MIT)](./LICENSE)
Copyright (c) 2016 YerevaNN
