# Shakesbot

Shakesbot is a single layer stateful Recurrent Neural Network for text generation, in the style of Shakespeare! Please visit <https://baknet.herokuapp.com/rnn/shakesbot> for an online demonstration of this model.

## Installation

TensorFlow and Numpy are required. To install the required dependencies to your current environment, run:

```bash
$ pip install -r requirements.txt
```

## shakesbot_train.py

This script will read the Shakespeare text provided, perform all the required mappings, create a model for training, train the model, then save a version of the model which can be used for testing. The arguments required for this script are as follows:

```python
python shakesbot_train.py GPU or CPU
```
Please specify when running the script whether you intend to train the model on GPU or CPU. Please be aware that training time varies vastly depending on this, with CPU training time being significantly longer.

This file will output shakesbot_train.h5 and shakesbot_test.h5, which are saved models from TensorFlow.

## shakesbot_test.py

This script allows a user to test the model, with a given input string, amount of characters to generate, and the "temperature" of the probabilities. 

Temperature scales from 1% to 200%, with the lower percentage generating much more predictable text.  

The amount of characters to generate (num_generate) has been limited to 2000 for the purposes of demonstration, however this can be changed manually from the script.  

The arguments required for this script are as follows:

```python
python shakesbot_test.py "start_seed" num_generate temperature
```
For example:
```python
python shakesbot_test.py "This is a test" 500 100
```

Produces output as such:

```
This is a testimony of the plainer
    of such a paragon. I shall see him and be the face of a
    speech, and the players of their death shall lose thee. Go, fellow,
    and therefore am not so long as thou art. Do you not
    think there was not the rest of thee to knock'd me to
    his hands? Is he underneath the fall and cheerful rock?
    The deadly stockings of the Spite of Troy,
    With all the last of them and the adventure of the state,
    That should be sure to see me light and look
```

## shakesbot.ipynb

This is a jupyter-notebook for step by step execution of training and testing the model. There are no limitations on the temperature and num_generate in this notebook.

## Example Models

Example test and train .h5 files have been provided. These have been trained on a GPU and therefore may require GPU enabled TensorFlow to utilise.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Author
My name is Benjamin Kavanagh, and I am an aspiring python developer. Please contact me at benjamin.a.kavanagh@gmail.com for any queries. 