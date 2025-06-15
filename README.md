---
type: "project"
date: "2025-06-15" 
# Title of your project (we like creative title)
title: "The Journey of Finding a N400"

# List the names of the collaborators within the [ ]. If alone, simple put your name within []
names: [Mei-Chun Kuo]

# Your project GitHub repository URL
github_repo:  https://github.com/mckuoling/Finding-a-N400-as-a-beginne

# List +- 4 keywords that best describe your project within []. Note that the project summary also involves a number of key words. Those are listed on top of the [github repository](https://github.com/PSY6983-2021/project_template), click `manage topics`.
# Please only lowercase letters
tags: [EEG, mne-python, n400, brainhack]

# Summarize your project in < ~75 words. This description will appear at the top of your page and on the list page with other projects..

summary: "Starting from the raw data, I adapted and translated the original EEGLAB (Matlab) script from ERP CORE into MNE-Python, making all the necessary modifications throughout the preprocessing pipeline to extract the N400."


---
<!-- This is an html comment and this won't appear in the rendered page. You are now editing the "content" area, the core of your description. Everything that you can do in markdown is allowed below. We added a couple of comments to guide your through documenting your progress. -->

## Project definition

### Background

As someone without much programming background and no prior experience with EEG experiments, I took on this project to gain hands-on experience working with raw EEG data — and to learn how to extract ERP components like the N400, which we often see in published studies.
The goal of the project was to use MNE-Python, the EEG analysis tool introduced in our course module. While the module provides a basic demonstration, it only covers some of the core steps. I wanted to understand the full pipeline, from raw data all the way through preprocessing.

### Tools

MNE-Python
The data preprocessing workflow: https://neuraldatascience.io/7-eeg/introduction.html

### Data

ERP CORE: N400 
https://erpinfo.org/erp-core

EEGLAB (Matlab) working pipline
https://github.com/mckuoling/ERP_CORE/tree/master/N400%20Analysis%20Files/N400/EEG_ERP_Processing


## Results

This is the N400 example produced by ERP CORE:
![ERP CORE Example N400](images/erp_core_n400.png)

(Kappenman et al, 2021)

And this is the N400 I generated using the same dataset, after adapting the original MATLAB pipeline to MNE-Python.
![My N400 Output](images/my_n400_result.png)


