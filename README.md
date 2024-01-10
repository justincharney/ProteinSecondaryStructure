# Protein Secondary Structure Prediction

The goal of this project was to create a seq2seq model that takes FASTA format inputs of amino acids and returns a sequence of 'H' and '-' characters indicating whether a given amino acid is part of an alpha-helix secondary structure.

For a more in-depth overview, please read the report: `BIEN_410_A3_Final.pdf`

## Example:
* Input amino acid sequence:
  ```
  SLFEQLGGQAAVQAVTAQFYANIQADATVATFFNGIDMPNQTNKTAAFLCAALGGPNAWTGRNLKEVHANMGVSNAQFTTVIGHLRSALTGAGVAAALVEQTVAVAETVRGDVVTV
  ```
* Predicted secondary structure
  ```
  H--HHH--HHHHHHHHHHHHHHHHH---H-HHHH---------HHHHHHHHHH----------HH---------HHHHHHHHHHHHHHHHH--HHHHHHHHHHHHHHHH-------
  ```

## Description

Training of several machine learning models (HMM, CNB, KNN, LSTM) is outlined in `/src/BIEN410_TrainingScripts.ipynb` and the results are summarized in the report `BIEN_410_A3_Final.pdf`.

## Getting Started

### Dependencies

* `NumPy` is the only required dependency for inference

### Installing

To clone this repository to your local machine, follow these steps:
* Open your terminal
* Navigate to the directory where you want to clone the repository
* Run the following git command
  ```
  git clone https://github.com/justincharney/ProteinSecondaryStructure.git
  ```

### Executing program
A small LSTM has been trained and the weights for the model + a dictionary used for tokenization of the input sequences has been saved to `/src/parameters.txt`

To run inference on an example input file `input_file/infile.txt` and compare the accuracy to the labels in `training_data/labels.txt`, complete the following:
* Navigate to `src/SSPred.py` and run the file. Predictions will be written to `output_file/outfile.txt`
* Navigate to `testing/testing.py` and run the file. The prediction accuracy will be displayed in the terminal

## Experimenting

If you wish to try another model, the Jupyter notebook `/src/BIEN410_TrainingScripts.ipynb` provides a starting point. Save a new parameters file after training your model and make any necessary modifications to the 
inference loop in `src/SSPred.py`

## Acknowledgments

This project was completed as a part of the coursework for BIEN 410 at McGill University.
This work is a result of the knowledge and skills acquired during the course and is guided by the principles and methodologies taught by Professor Brandon Xia.
