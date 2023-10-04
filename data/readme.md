## Data
Keep your data (e.g. from evaluations here)


* If you involved human subjects in any form, you will require ethical permission.
    * Keep records of all items related to ethics in `data/ethics`. There are templates for scripts, guidance provided.
    * **You must have scanned PDFs of signed checklists in this folder**, or PDFs of ethics confirmations from other sources
    * Ensure you remain GDPR compliant. In general:
        * Never collect personally identifiable information if at all possible. 
        * Pseudonymise identifiers for subjects. 
        * Use coarse demographic values unless you need specific information (for example, if you need age ranges, collect ranges, not specific ages)
        * Ensure you have explicit consent for the storage and use of data from human subjects
        * DO NOT STORE PERSONALLY IDENTIFIABLE INFORMATION ON REMOTE SERVERS (no Dropbox, Github, etc.)

* Keep a written description of the data, what is contained, and how it was captured in `data/readme.md`
* Record all raw data as an immutable store. **Never modify captured data.** 
    * Keep this under `data/raw`
    * This could be logs, questionnaire responses, computation results

* Write scripts to produced processed data from these (e.g. tidy dataframes, excel sheets, csv files, HDF5 files, sqlite databases)
* Write scripts that process these into results, visualisations, tables that you include in your project.
* If you use Jupyter/RStudio notebooks, place these in `data/notebooks` and name them carefully (not "Untitled1", "Untitled2").

* You may need to remove the `data/` folder from version control if the data size is too large or you are bound by confidentiality.
* If you do so **make sure you have good backups**

### Data source

Used data is the RAVDESS data set, downloaded from https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio?resource=download
Livingstone SR, Russo FA (2018) The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS): A dynamic, multimodal set of facial and vocal expressions in North American English. PLoS ONE 13(5): e0196391. https://doi.org/10.1371/journal.pone.0196391.
The following two sections are copied from the website.

### Data structure

This portion of the RAVDESS contains 1440 files: 60 trials per actor x 24 actors = 1440. The RAVDESS contains 24 professional actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent. Speech emotions includes calm, happy, sad, angry, fearful, surprise, and disgust expressions. Each expression is produced at two levels of emotional intensity (normal, strong), with an additional neutral expression.

### File names

Each of the 1440 files has a unique filename. The filename consists of a 7-part numerical identifier (e.g., 03-01-06-01-02-01-12.wav). These identifiers define the stimulus characteristics:

Filename identifiers

* Modality (01 = full-AV, 02 = video-only, 03 = audio-only).
* Vocal channel (01 = speech, 02 = song).
* Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised).
* Emotional intensity (01 = normal, 02 = strong). NOTE: There is no strong intensity for the 'neutral' emotion.
* Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").
* Repetition (01 = 1st repetition, 02 = 2nd repetition).
* Actor (01 to 24. Odd numbered actors are male, even numbered actors are female).

_Filename example: 03-01-06-01-02-01-12.wav_

* Audio-only (03)
* Speech (01)
* Fearful (06)
* Normal intensity (01)
* Statement "dogs" (02)
* 1st Repetition (01)
* 12th Actor (12)
* Female, as the actor ID number is even.