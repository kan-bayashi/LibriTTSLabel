# Word / phone alignment label for LibriTTS Corpus

This repository provides word / phone alignment labels for [LibriTTS Corpus](https://arxiv.org/abs/1904.02882).

The label files are created by [Montreal-Forced-Aligner](https://github.com/MontrealCorpusTools/Montreal-Forced-Aligner) with provided pretrained model.


## Missing files

Due to the alignment failures, some labels are missing (around 0.4 %).  
Please check `missing_files.txt`


## Data structure

This repository provides two types of alignments files:  
1) `.lab` format separated with "\t",  
2) `.TextGrid` format, which the raw outputs of MFA.

`.lab` files are prepared for `phone` and `word` while `.TextGrid` includes both in a single file.

```
lab
├── phone
│   ├── dev-clean
│   ├── dev-other
│   ├── test-clean
│   ├── test-other
│   ├── train-clean-100
│   ├── train-clean-360
│   └── train-other-500
├── word
│   ├── dev-clean
│   ├── dev-other
│   ├── test-clean
│   ├── test-other
│   ├── train-clean-100
│   ├── train-clean-360
│   └── train-other-500
textgrid
├── dev-clean
├── dev-other
├── test-clean
├── test-other
├── train-clean-100
├── train-clean-360
└── train-other-500
```

## Label format

### Word label

```
0.0     0.03
0.03    0.4     matthew
0.4     0.84    cuthbert
0.84    0.87
0.87    0.99    is
0.99    1.59    surprised
1.59    1.67
```

### Phone label

```
0.0     0.03    sil
0.03    0.13    M
0.13    0.23    AE1
0.23    0.28    TH
0.28    0.34    Y
0.34    0.4     UW0
0.4     0.48    K
0.48    0.56    AH1
0.56    0.65    TH
0.65    0.71    B
0.71    0.8     ER0
0.8     0.84    T
0.84    0.87    sp
0.87    0.95    IH1
0.95    0.99    Z
0.99    1.05    S
1.05    1.1     AH0
1.1     1.17    P
1.17    1.25    R
1.25    1.38    AY1
1.38    1.5     Z
1.5     1.59    D
1.59    1.65    sp
1.65    1.67
```

### TextGrid

```
File type = "ooTextFile"
Object class = "TextGrid"

xmin = 0.0
xmax = 1.67
tiers? <exists>
size = 2
item []:
        item [1]:
                class = "IntervalTier"
                name = "words"
                xmin = 0.0
                xmax = 1.67
                intervals: size = 7
                        intervals [1]:
                                xmin = 0.0
                                xmax = 0.030
                                text = ""
                        intervals [2]:
                                xmin = 0.030
                                xmax = 0.400
                                text = "matthew"
                        intervals [3]:
                                xmin = 0.400
                                xmax = 0.840
                                text = "cuthbert"
                        intervals [4]:
                                xmin = 0.840
                                xmax = 0.870
                                text = ""
                        intervals [5]:
                                xmin = 0.870
                                xmax = 0.990
                                text = "is"
                        intervals [6]:
                                xmin = 0.990
                                xmax = 1.590
                                text = "surprised"
                        intervals [7]:
                                xmin = 1.590
                                xmax = 1.67
                                text = ""
        item [2]:
                class = "IntervalTier"
                name = "phones"
                xmin = 0.0
                xmax = 1.67
                intervals: size = 24
                        intervals [1]:
                                xmin = 0.000
                                xmax = 0.030
                                text = "sil"
                        intervals [2]:
                                xmin = 0.030
                                xmax = 0.130
                                text = "M"
                        intervals [3]:
                                xmin = 0.130
                                xmax = 0.230
                                text = "AE1"
                        intervals [4]:
                                xmin = 0.230
                                xmax = 0.280
                                text = "TH"
                        intervals [5]:
                                xmin = 0.280
                                xmax = 0.340
                                text = "Y"
                        intervals [6]:
                                xmin = 0.340
                                xmax = 0.400
                                text = "UW0"
                        intervals [7]:
                                xmin = 0.400
                                xmax = 0.480
                                text = "K"
                        intervals [8]:
                                xmin = 0.480
                                xmax = 0.560
                                text = "AH1"
                        intervals [9]:
                                xmin = 0.560
                                xmax = 0.650
                                text = "TH"
                        intervals [10]:
                                xmin = 0.650
                                xmax = 0.710
                                text = "B"
                        intervals [11]:
                                xmin = 0.710
                                xmax = 0.800
                                text = "ER0"
                        intervals [12]:
                                xmin = 0.800
                                xmax = 0.840
                                text = "T"
                        intervals [13]:
                                xmin = 0.840
                                xmax = 0.870
                                text = "sp"
                        intervals [14]:
                                xmin = 0.870
                                xmax = 0.950
                                text = "IH1"
                        intervals [15]:
                                xmin = 0.950
                                xmax = 0.990
                                text = "Z"
                        intervals [16]:
                                xmin = 0.990
                                xmax = 1.050
                                text = "S"
                        intervals [17]:
                                xmin = 1.050
                                xmax = 1.100
                                text = "AH0"
                        intervals [18]:
                                xmin = 1.100
                                xmax = 1.170
                                text = "P"
                        intervals [19]:
                                xmin = 1.170
                                xmax = 1.250
                                text = "R"
                        intervals [20]:
                                xmin = 1.250
                                xmax = 1.380
                                text = "AY1"
                        intervals [21]:
                                xmin = 1.380
                                xmax = 1.500
                                text = "Z"
                        intervals [22]:
                                xmin = 1.500
                                xmax = 1.590
                                text = "D"
                        intervals [23]:
                                xmin = 1.590
                                xmax = 1.650
                                text = "sp"
                        intervals [24]:
                                xmin = 1.650
                                xmax = 1.67
                                text = ""
```

For details, please check [MFA document](https://montreal-forced-aligner.readthedocs.io/en/latest/).

## Reference

- [LibriTTS Corpus](https://arxiv.org/abs/1904.02882)
- [Montreal-Forced-Aligner](https://github.com/MontrealCorpusTools/Montreal-Forced-Aligner)
