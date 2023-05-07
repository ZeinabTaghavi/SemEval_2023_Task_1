# SemEval_2023_Task_1
# Visual Word Sense Disambiguation Using CLIP

This repository contains the code and resources for a Visual Word Sense Disambiguation (Visual-WSD) system that utilizes the state-of-the-art CLIP model for zero-shot image classification and retrieval. The system compares various methods and evaluates their performance on a Visual-WSD task.

## Overview

The main goal of this project is to disambiguate word senses using images and textual contexts. We explore the benefits of cross-modality evaluation between text and candidate images using CLIP encoders for both input text and images. Additionally, we investigate the potential of prompt engineering and text-to-image models, such as DALL-E 2 and GLIDE, to improve accuracy in Visual-WSD tasks.

## Dependencies

- Python 3.7+
- PyTorch
- OpenAI's CLIP
- OpenAI's DALL-E 2
- GLIDE
- NumPy
- SciPy

## Dataset

The dataset used in this project is an image selection task that requires choosing an image corresponding to a given word and limited textual context. The dataset is not provided in this repository, but you can create your own or use a publicly available dataset suitable for Visual-WSD tasks.

## Experiment Setup

The experiments involve two types of prompts:

1. Simple prompts: Concatenating the word and limited textual context to create a text prompt.
2. Generated prompts: Using OpenAI's "text-davinci-003" Completion model to generate prompts by adding the phrase ", can you describe it as a picture?" to the end of the Simple prompts.

Two text-to-image models, GLIDE and DALL-E 2, are used to generate images from the text prompts. The generated images and candidate images are then processed using the "ViT-B/32" CLIP model to obtain embeddings. Cosine similarity is used to compare the embeddings and determine the closest image to the input text.

## Usage

1. Clone the repository.
2. Install the required dependencies.
3. Prepare your dataset and configure the paths in the `config.py` file.
4. Run the experiments in jupyter notebook.

## Acknowledgements

We would like to thank the creators of the CLIP, DALL-E 2, and GLIDE models, as well as the open-source community for their valuable resources.

## Contact

If you have any questions or suggestions, please feel free to open an issue or submit a pull request.

