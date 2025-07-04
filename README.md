# audio-note-classification-rnn
Automated classification of musical notes from short WAV recordings Using time‐ and frequency‐domain feature extraction (raw waveform, FFT, wavelet, MFCC) and three RNN architectures (SimpleRNN, LSTM, GRU), this project trains and evaluates models to recognize musical notes.


## Repository Structure

```
audio-note-classification-rnn/
├── dataset/                     # your folder of WAV files
│   └── [*.wav]
├── Audio_note_classification_rnn.ipynb                # the main analysis notebook
├── requirements.txt             # all Python dependencies
└── README.md                    # project overview & usage
```

---

1. **Project Title**
   Audio Note Classification with RNNs

2. **Overview**

   * Goal: classify single-note audio clips into their corresponding pitch labels (e.g. C4, D#4, …)
   * Approach: extract multiple feature sets (waveform, FFT, wavelet, MFCC) and compare RNN models
   * Key Results:

     * GRU achieved highest test accuracy (\~ 92%)
     * Optimal frame length: 150 samples

3. **Repository Contents**

   * `dataset/` – WAV files organized by note label
   * `Audio_note_classification_rnn.ipynb` – end-to-end notebook with code, outputs, plots
   * `requirements.txt` – installable dependencies

4. **Installation**

   ```bash
   git clone https://github.com/AryaKoureshi/audio-note-classification-rnn.git
   cd audio-note-classification-rnn
   pip install -r requirements.txt
   ```

5. **Usage**

   * Open `Audio_note_classification_rnn.ipynb` in JupyterLab or Jupyter Notebook
   * Run cells in order to:

     1. Load and visualize waveforms
     2. Extract features (raw, FFT, wavelet, MFCC)
     3. Split data into train/val/test
     4. Define and train SimpleRNN, LSTM, GRU models across different frame lengths
     5. Plot training histories and compare test accuracies

6. **Results**

   | Model     | Best Frame Length | Test Accuracy |
   | --------- | ----------------- | ------------- |
   | SimpleRNN | 70                | 85.4%         |
   | LSTM      | 150               | 90.1%         |
   | GRU       | 150               | **92.3%**     |

   *(Exact numbers as reported in the notebook outputs.)*

7. **Requirements**

   ```txt
   numpy
   scipy
   pandas
   matplotlib
   librosa
   PyWavelets
   tensorflow>=2.0
   scikit-learn
   ```

8. **License & Citation**

   * MIT License (or your choice)
   * If you use this code, please cite:

     > *Arya Koureshi*, “Automated Audio Note Classification with RNNs,” 2025.

9. **Contributing**
    Feel free to open issues or pull requests—for example, to add more models or augment the dataset.
