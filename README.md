
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/fadymedhat/GTZAN-for-MCLNN/blob/master/LICENSE)

# Ballroom dataset for MCLNN

The Ballroom dataset was used in the [ISMIR2004 tempo induction contest](http://mtg.upf.edu/ismir2004/contest/tempoContest/).
The dataset music clips can be downloaded from [here](http://mtg.upf.edu//ismir2004/contest/tempoContest/node5.html).

| Clip Duration  | Format | Count | Categories|
|:---:|:---:|:---:|:---:|
| 30 secs | .wav | 698 | 8 |

Dataset Summary:
 * clips are 30 seconds in length with 44100 Hz sampling rates.
 * No predefined split is defined for the dataset cross-validation.

 
 This folder contains:
  * Pretrained weights and indices for the 10-fold cross-validation in addition to the standardization parameters to replicate the results in:
  
 _Fady Medhat, David Chesmore and John Robinson, "Automatic Classification of Music Genre Using Masked Conditional Neural Networks," 2017 IEEE International Conference on Data Mining (ICDM)_
 
 ## Prepossessing
 
The preprocessing involved in preparing the Ballroom dataset is resampling to .wav at 22050 Hz (note: resampling is done through librosa while transforming the clips to spectrograms).

 
#### Steps
1. Make sure the files are ordered following the [Ballroom_storage_ordering](https://github.com/fadymedhat/Ballroom-for-MCLNN/blob/master/ballroom_storage_ordering.txt) file.
2. Configure the spectrogram transformation within the [Dataset Transformer](https://github.com/fadymedhat/MCLNN/tree/master/dataset_transformer) and generate the MCLNN-Ready hdf5 for the dataset.
3. Generate the indices for the folds using the [Index Generator](https://github.com/fadymedhat/MCLNN/tree/master/index_generator) script.

