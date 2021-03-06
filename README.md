## BembaSpeech ASR Corpus

If you use this speech dataset in your project or research, please consider citing:

    @inproceedings{sikasote-anastasopoulos21bembaspeech,
        abstract = {We present a preprocessed, ready-to-use automatic speech recognition corpus, BembaSpeech, consisting over 24 hours of read speech in the Bemba language, a written but low-resourced language spoken by over 30% of the population in Zambia. To assess its usefulness for training and testing ASR systems for Bemba, we train an end-to-end Bemba ASR system by fine-tuning a pre-trained DeepSpeech English model on the training portion of the BembaSpeech corpus. Our best model achieves a word error rate (WER) of 54.78%. The results show that the corpus can be used for building ASR systems for Bemba.},
        title = {BembaSpeech: A Speech Recognition Corpus for the Bemba Language},
        author = {Sikasote, Claytone and Anastasopoulos, Antonios},
        booktitle = {Proceedings of AfricaNLP},
        address = {Online},
        month = {April},
        year = {2021},
        url = {https://arxiv.org/pdf/2102.04889.pdf}
    }

-----------------

1. INTRODUCTION

----------------------

BembaSpeech is a corpus of read speech in Bemba language of Zambia, based on publicly available Bemba literature books. Its purpose is to enable the training and testing of automatic speech recognition(ASR) systems in Bemba language. The corpus has 14, 438 utterances culminating into 24.5 hours of speech data.

All signal files are encoded in Waveform Audio File Format (WAVE) from a mono recording with a sample rate of 16K Hz.

2. STRUCTURE

-------------

The corpus is split into three parts:

* [train](BembaSpeech/train) - training set, of approximately 20 hours of speech 
* [dev](BembaSpeech/dev)   - development set, of approximately 2.5 hours of speech
* [test](BembaSpeech/test)  - testing set, of approximately 2 hours of speech

These subsets are disjoint, i.e. the audio of each speaker is assigned to exactly one subset. The allocation of each speaker contribution is as follows:

    _____________________________________________________________________________________________
    | NAME  | DURATION |  UNITS | 		SPEAKERS		|   Male   |    Female      |
    _____________________________________________________________________________________________
    | Train | 20:05:09 | 11,906 | 01, 03, 04, 05, 07, 08, 09, 10	|      5   |       3        |
    .--------------------------------------------------------------------------------------------
    | Dev	| 02:27:20 | 1,555  | 02, 11, 13, 14, 15, 16, 17	|      3   |       4        | 
    .--------------------------------------------------------------------------------------------
    | Test	| 02:03:03 | 977    | 06, 12				|      1   |       1        |
    ---------------------------------------------------------------------------------------------
    

3. FILE ORGANIZATION

----------------
The corpus file organization is as follows:

    <BembaSpeech>
        |
        .- DATASTATEMENT.md
        |
        .- README.TXT
        |
        .- SPEAKERS.TXT
        |
        .- train -/
        |        |
        .        .- 01 - /
        |           |
        .           .- 180101-020137_bem_d31_elicit - /
        |           |	    |
        .           .	    .- 01-180101-020137_bem_d31_elicit_text_script.txt
        |           |	    |
        .           .	    .- 01-180101-020137_bem_d31_elicit_transcript.txt
        |           |	    |    
        .           .	    .- 01-180101-020137_bem_d31_elicit_0.wav
        |           |	    |
        .           .	    .- 01-180101-020137_bem_d31_elicit_1.wav
        |           |	    |
        .           |	    . ...
        |           |
        .           .- 180101-020249_bem_d31_elicit/
        |           	    |
        . ...                   .- ...
               	    

------------------
* [train](BembaSpeech/train) - is the train dataset subset name
* **01**    - is the speaker_id of the speaker
* **180101-020249_bem_d31_elicit** is the recording session of the speaker. 
* **\*_transcripts.txt** files contains the transcripts for each of the utterances [<utterance_id transcript>]. 
* **\*_text_script.txt** files contains the text from which readers read from to create audio. <transcripts>
* [SPEAKERS.TXT](BembaSpeech/SPEAKERS.TXT) contains speaker information and their contributuion to the corpus.
* [DATASTATEMENT](DATASTATEMENT.md) has contextual information to the creation of this dataset in detail
